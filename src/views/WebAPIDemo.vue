<template>
  <div>
    <div>
      <h6>Get bike station List</h6>
      <RegresAllBike :error="axioError" :allData="axioAllData" />
    </div>
  </div>
</template>

<script>
import RegresAllBike from '@/components/RegresAllBike.vue';
import axios from 'axios';
const API_URL = 'https://tdx.transportdata.tw/api/basic/';
export default {
  data() {
    return {
      axioError: false,
      axioAllData: [],
      city: 'Taoyuan',
      params: {
        format: 'JSON',
      },
      accesstoken: '',
    };
  },
  components: {
    RegresAllBike,
  },
  async mounted() {
    await this.getAuthorizationHeader();
    await this.AxiosFunc();
  },
  methods: {
    getAuthorizationHeader() {
      const AUTH_URL =
        'https://tdx.transportdata.tw/auth/realms/TDXConnect/protocol/openid-connect/token';
      const parameter = new URLSearchParams();
      parameter.append('grant_type', 'client_credentials');
      parameter.append('client_id', 'leon.lu3303-40eeecc2-818b-4488');
      parameter.append('client_secret', '62861a42-e9e7-4086-ae49-d91e5c8d1e5d');

      return axios({
        method: 'POST',
        url: AUTH_URL,
        headers: { 'content-type': 'application/x-www-form-urlencoded' },
        data: parameter,
      })
        .then((response) => {
          this.accesstoken = response.data;
        })
        .catch((err) => {
          this.axioError = true;
        });
    },
    AxiosFunc() {
      if (!(this.accesstoken && this.accesstoken.access_token)) return;
      this.axioAllData = [];
      return axios
        .get(`${API_URL}v2/Bike/Station/City/${this.city}`, {
          headers: {
            authorization: `Bearer ${this.accesstoken.access_token}`,
          },
          params: this.params,
        })
        .then((response) => {
          this.axioError = response.status !== 200;
          this.axioAllData = response.data;
        })
        .catch((err) => {
          this.axioError = true;
        });
    },
  },
};
</script>

<style lang="scss" scoped>
.pagination {
  button {
    cursor: pointer;
    margin: 3px;
    &:hover {
      background: #ddd;
    }
    &.active {
      background: #999;
    }
  }
}
h6 {
  font-size: 48px;
  font-weight: 600;
}
</style>
