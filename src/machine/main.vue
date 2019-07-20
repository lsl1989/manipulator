<template>
  <div class="machine-page">
    <div class="title">产线运行状态</div>
    <div class="machine-map">
      <div class="machine-body">
        <div class="machine-box-container">
          <div class="machine-box working">
            <i class="right-light"></i>
            <i class="box"></i>
          </div>
          <div class="machine-box">
            <i class="right-light"></i>
            <i class="box"></i>
          </div>
          <div class="machine-box">
            <i class="right-light"></i>
            <i class="box"></i>
          </div>
        </div>
        <div class="machine-sweet-container clearfix">
          <div class="machine-sweet working">
            <i class="bottom-light"></i>
            <i class="sweet-push"></i>
            <i class="sweet"></i>
            <i class="opposite">
              <i class="sweet-push-opposite"></i>
            </i>
          </div>
          <div class="machine-sweet working">
            <i class="bottom-light"></i>
            <i class="sweet-push"></i>
            <i class="sweet"></i>
            <i class="opposite">
              <i class="sweet-push-opposite"></i>
            </i>
          </div>
          <div class="machine-sweet">
            <i class="bottom-light"></i>
            <i class="sweet-push"></i>
            <i class="sweet"></i>
            <i class="opposite">
              <i class="sweet-push-opposite"></i>
            </i>
          </div>
          <div class="machine-sweet">
            <i class="bottom-light"></i>
            <i class="sweet-push"></i>
            <i class="sweet"></i>
            <i class="opposite">
              <i class="sweet-push-opposite"></i>
            </i>
          </div>
          <div class="machine-sweet">
            <i class="bottom-light"></i>
            <i class="sweet-push"></i>
            <i class="sweet"></i>
            <i class="opposite">
              <i class="sweet-push-opposite"></i>
            </i>
          </div>
          <div class="machine-sweet">
            <i class="bottom-light"></i>
            <i class="sweet-push"></i>
            <i class="sweet"></i>
            <i class="opposite">
              <i class="sweet-push-opposite"></i>
            </i>
          </div>
        </div>
        <div class="machine-lid-container clearfix">
          <div class="machine-lid working">
            <i class="bottom-light"></i>
            <i class="lid-push"></i>
            <i class="lid"></i>
          </div>
          <div class="machine-lid working">
            <i class="bottom-light"></i>
            <i class="lid-push"></i>
            <i class="lid"></i>
          </div>
          <div class="machine-lid working">
            <i class="bottom-light"></i>
            <i class="lid-push"></i>
            <i class="lid"></i>
          </div>
        </div>
        <div class="mounting working">
          <i class="box-push-container">
            <i class="box-push"></i>
          </i>
          <i class="box"></i>
          <i class="lid"></i>
        </div>
        <six-axis-arm className="six-axis-arm" :working="true" arm_type="lid_arm">
          <div class="lid" slot="captured"></div>
        </six-axis-arm>
        <six-axis-arm className="six-axis-arm-push" :working="true" arm_type="push_arm">
          <div class="slot-container" slot="captured">
            <i class="box">
              <i class="lid"></i>
            </i>
            <i class="star-five"></i>
          </div>
        </six-axis-arm>
        <div class="unloading working">
          <i class="left-light"></i>
          <i class="push"></i>
          <i class="box">
            <i class="lid"></i>
          </i>
          <i class="unloading-area"></i>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
  import './index.scss'
  import SixAxisArm from './six_axis_arm.vue'

  export default {
    name: 'machine',
    components: {
      'six-axis-arm': SixAxisArm
    },
    data: function () {
      return {
        machine_state: 'start'
      }
    }
  }
</script>