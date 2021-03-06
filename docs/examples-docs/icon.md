<style>
.demo-icon {
  font-size: 0;

  .examples {
    max-height: none;
  }

  .van-col {
    text-align: center;
    height: 100px;
    float: none;
    display: inline-block;
    color: rgba(69, 90, 100, .8);
  }

  .van-icon {
    font-size: 32px;
    margin: 15px 0;
    display: block;
  }

  span {
    font-size: 14px;
  }
} 
</style>

<script>
import Vue from 'vue';
import { Icon } from 'packages';

const icons = [
  'close',
  'location',
  'clock',
  'gold-coin',
  'chat',
  'exchange',
  'upgrade',
  'edit',
  'contact',
  'passed',
  'points',
  'delete',
  'records',
  'logistics',
  'check',
  'checked',
  'gift',
  'like-o',
  'like',
  'qr',
  'qr-invalid',
  'shop',
  'photograph',
  'add',
  'add2',
  'photo',
  'cart',
  'arrow',
  'search',
  'clear',
  'success',
  'fail',
  'wechat',
  'alipay',
  'password-view',
  'wap-nav',
  'password-not-view',
  'wap-home',
  'ecard-pay',
  'balance-pay',
  'peer-pay',
  'credit-pay',
  'debit-pay',
  'other-pay',
  'cart',
  'browsing-history',
  'goods-collect',
  'shop-collect',
  'receive-gift',
  'send-gift',
  'setting',
  'coupon',
  'free-postage',
  'discount',
  'birthday-privilege',
  'member-day-privilege',
  'balance-details',
  'cash-back-record',
  'points-mall',
  'exchange-record',
  'pending-payment',
  'pending-orders',
  'pending-deliver',
  'pending-evaluate',
  'cash-on-deliver',
  'gift-card-pay',
  'underway',
  'point-gift',
  'after-sale',
  'edit-data',
  'question',
  'description',
  'card',
  'gift-card',
  'coupon'
];

Vue.component('van-icon-inner', Icon);
Vue.component('van-icon', {
  props: ['name'],

  render(h) {
    return (
      <div>
        {icons.map(icon => (
          <van-col span="8">
            <van-icon-inner name={icon}></van-icon-inner>
            <span>{icon}</span>
          </van-col>
        ))}
      </div>
    )
  }
});

export default {};
</script>

## Icon 图标

### 使用指南
``` javascript
import { Icon } from 'vant';

Vue.component(Icon.name, Icon);
```

### 代码演示

#### 基础用法

设置`name`属性为对应的图标名称即可，所有可用的图标名称见右侧列表

:::demo 基础用法
```html
<van-icon name="success"></van-icon>
```
:::

### API

| 参数       | 说明      | 类型       | 默认值       | 可选值       |
|-----------|-----------|-----------|-------------|-------------|
| name | icon名称 | `String`  | `''` | - |
