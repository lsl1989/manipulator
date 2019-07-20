<template>
  <div :class="className">
    <div class="arm-base" :class="[{[arm_type]: arm_type, working: working}]">
      <div class="arm-section arm-section-1">
        <div class="arm-section arm-section-2">
          <div class="arm-section arm-section-3">
            <div class="arm-section arm-section-4">
              <div class="arm-claw">
                <slot name="captured"></slot>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  import './six_axis_arm.scss'
  /*
  * 四轴机械臂。
  * 组成部分：底座，机械手一段，二段，三段，四段，机械爪
  * 控制参数：
  * 1. 启停参数
  * 2. 四段机械手初始朝向角度
  * 3. 动画时长
  * 4. 四段机械手变幻路径数组，最后一个值为最终落点 (JS控制keyframes可能会有问题，所以采用写死2套运动轨迹的方式)
  * 5. 机械手是否原路返回 ？
  * 6. 返回路径数组 ？
  * 7. 两种模式，lid_arm, push_arm
  * */
  export default {
    props: {
      className: {
        'type': String,
        'default': '',
      },
      working: {
        'type': Boolean,
        'default': false,
      },
      arm_route: Array,
      reset_original: {
        'type': Boolean,
        'default': true,
      },
      reset_route: Array,
      arm_type: {
        'type': String,
        'default': 'lid_arm', // lid_arm or push_arm
      }
    },
    data: function () {
      return {
      }
    }
  }
</script>
