<template>
  <div>
    <ul>
      <item-view>
        아이템 1
        <div slot="body">
          아이템 1 바디
          <button>click me</button>
        </div>
      </item-view>
      <item-view>
        아이템 2
          <div slot="header">
            헤더
          </div>
          <div slot="footer">
            푸터
          </div>
      </item-view>
      <item-view>아이템 3</item-view>
      <item-view>아이템 4</item-view>
      <item-view>아이템 5</item-view>
    </ul>
  </div>
</template>

<script>
import ItemView from './components/ItemView.vue'

export default {
  components: { ItemView },

}
</script>

<style>

</style>