<div class="view">
  <div class="chanel">
    <ul>
      <li v-for="channel in channels">
        <router-link :to="{ name: 'channel', params: { cname: channel } }">
          {{ channel }}
        </router-link>
      </li>
    </ul>
  </div>

  <div class="channel-name">
    {{ $route.params.cname }}
  </div>

  <div class="messages">
    <ul>
      <li v-for="mes in messages">{{ mes }}</li>
    </ul>
  </div>

  <div class="form">
    <input type="text" v-model="message">
    <input type="button" value="送信する" @click="send_message">
  </div>

</div>

