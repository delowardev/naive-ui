# 日期
```html
<n-date-picker
  v-model="timestamp"
  type="date"
  :disabledTime="disabledTime"
  clearable
/>
<n-date-picker v-model="timestamp2" type="date" clearable />
<pre>{{ JSON.stringify(timestamp) }}, {{ JSON.stringify(timestamp2) }}</pre>
```
```js
export default {
  data () {
    return {
      timestamp: null,
      timestamp2: 1000000
    }
  },
  methods: {
    disabledTime (current) {
      return (current >= 1574092800000) && (current < 1574438400000)
    }
  }
}
```
```css
.n-date-picker {
  margin: 0 12px 8px 0;
}
```