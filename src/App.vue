<script setup>
const stats = [
  { value: '5', label: '已上线平台', unit: '个' },
  { value: '5', label: '覆盖业务场景', unit: '类' },
  { value: '1', label: '统一入口', unit: '个' },
]

const platforms = [
  {
    name: '业务督导中心数智化管理平台',
    url: 'https://ywddzx.com',
    scene: '巡检管理',
    description: '面向巡检登记、整改复核、规范库和记录追踪的统一工作入口。',
    status: '已上线',
  },
  {
    name: '签训通',
    url: 'https://qxt.ywddzx.com',
    scene: '培训签署',
    description: '面向培训文件签署、员工确认、培训记录和签名留痕的在线签训系统。',
    status: '已上线',
  },
  {
    name: '民主测评管理系统',
    url: 'https://mzcp.ywddzx.com',
    scene: '民主测评',
    description: '面向巡察组任务管理、二维码测评、进度统计和满意度分析的测评系统。',
    status: '已上线',
  },
  {
    name: 'SmartPlateX 智能车牌识别系统',
    url: 'https://spx.ywddzx.com',
    scene: '智能识别',
    description: '面向视频上传、抽帧识别、车牌统计和车辆类型分析的智能识别系统。',
    status: '已上线',
  },
  {
    name: '油客智荐',
    url: 'https://youke.ywddzx.com/',
    scene: '会员营销',
    description: '会员下次购买预测系统，基于会员消费序列学习，预测客户下次购买行为，支撑油站会员智能营销演示。',
    status: '已上线',
  },
]
</script>

<template>
  <main class="portal-shell">
    <section class="hero-section" aria-labelledby="portal-title">
      <div class="hero-content">
        <p class="eyebrow">home.ywddzx.com</p>
        <h1 id="portal-title">业务督导中心数智化平台门户</h1>
        <p class="hero-subtitle">
          汇聚巡检管理、培训签署、民主测评、智能识别、会员营销等应用，打造统一、高效、可持续扩展的数智化工作入口。
        </p>

        <div class="stats-panel" aria-label="平台统计">
          <div v-for="item in stats" :key="item.label" class="stat-item">
            <strong>
              {{ item.value }}
              <small>{{ item.unit }}</small>
            </strong>
            <span>{{ item.label }}</span>
          </div>
        </div>
      </div>
    </section>

    <section class="platform-section" aria-labelledby="platform-title">
      <div class="section-heading">
        <p class="eyebrow">统一应用入口</p>
        <h2 id="platform-title">平台入口</h2>
      </div>

      <div class="platform-grid">
        <a
          v-for="platform in platforms"
          :key="platform.url"
          class="platform-card"
          :href="platform.url"
          target="_blank"
          rel="noopener noreferrer"
          :aria-label="`进入${platform.name}`"
        >
          <span class="status-badge">{{ platform.status }}</span>
          <div class="card-icon" aria-hidden="true">{{ platform.scene.slice(0, 2) }}</div>
          <div class="card-body">
            <p class="scene-label">{{ platform.scene }}</p>
            <h3>{{ platform.name }}</h3>
            <p>{{ platform.description }}</p>
          </div>
          <span class="enter-button">
            进入系统
            <span aria-hidden="true">→</span>
          </span>
        </a>
      </div>
    </section>

    <footer class="portal-footer">
      <span>数智化平台门户 v1.0</span>
    </footer>
  </main>
</template>
