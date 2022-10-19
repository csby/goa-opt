<script>
import Component from 'vue-class-component'
import VueBase from '@/components/VueBase'

@Component
class SocketBase extends VueBase {
  sendSocketMessage (id, data) {
    this.$evt.fire(this.$evt.local.socket, id, data)
  }

  connected () {
  }

  onSocketMessage (id, data) {
  }

  onSocketConnected () {
    this.connected()
  }

  onSocketNotify (id, data) {
    this.onSocketMessage(id, data)
  }

  mounted () {
    this.$evt.on(this.$evt.websocket.connected, this.onSocketConnected)
    this.$evt.on(this.$evt.websocket.notify, this.onSocketNotify)

    if (this.$db.get(this.$db.keys.connected)) {
      this.connected()
    }
  }

  beforeDestroy () {
    this.$evt.off(this.$evt.websocket.notify, this.onSocketNotify)
    this.$evt.off(this.$evt.websocket.connected, this.onSocketConnected)
  }
}

export default SocketBase
</script>
