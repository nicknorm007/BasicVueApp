<template>
<div>
  <div class="box">
    <a class="button is-info" @click="getBuildJson(dev)">Dev Env Info</a>
    <a class="button is-warning" @click="getBuildJson(qa)">QA Env Info</a>
    <a class="button is-success" @click="getBuildJson(stg)">STG Env Info</a>
    <a class="button is-danger" @click="getBuildJson(prd)">PROD Env Info</a>
  </div>
  </br>
  </br>
  <div class="results">
    <table class="table is-bordered is-striped is-narrow">
      <thead>
        <tr>
          <th>SHA</th>
          <th>Build</th>
          <th>Branch</th>
          <th>Version</th>
          <th>Build Date</th>
          <th>Build Num</th>
        </tr>
      </thead>
        <tbody>
          <tr>
            <td>{{ envInfo.sha }}</td>
            <td>build</td>
            <td>branch</td>
            <td>version</td>
            <td>builddate</td>
            <td>buildnum</td>
          </tr>
        </tbody>
      </table>
  </div>
</div>
</template>

<script>

  import axios from 'axios';

  export default {
    name: 'simple-env',
    data: function () {
      return {
        qa: 'https://qa-authoring.i-ready.com/build-info.json',
        dev: 'https://dev-authoring.i-ready.com/build-info.json',
        stg: '',
        prod: '',
        envInfo: {sha : '', build : '', branch: '', version: '',
                  buildDate: '', buildNum: ''}
      }
    },
    methods: {
      getBuildJson: function(url) {

        axios.get(url)
          .then(response => {
            let data = response.data;
            this.envInfo['sha'] = data['git']['sha'];
          })
          .catch(error => {
            console.log(error);
          });
      },
    }
}
</script>
