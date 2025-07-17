<script lang="ts">
  import { Heart, Mic, Gift, Lock, Zap, BarChart3 } from 'lucide-svelte';
  
  const features = [
    {
      icon: Heart,
      title: '호감도 시스템',
      description: '대화할수록 높아지는 친밀도! 특별한 콘텐츠와 이벤트를 해금하세요.',
      color: 'text-pink-400',
      bgColor: 'bg-pink-500/10'
    },
    {
      icon: Mic,
      title: '음성 대화',
      description: 'Supertone API로 크리에이터의 실제 목소리를 학습한 자연스러운 대화',
      color: 'text-blue-400',
      bgColor: 'bg-blue-500/10'
    },
    {
      icon: Gift,
      title: '선물 & 후원',
      description: '캐릭터에게 보낸 선물이 크리에이터에게 직접 전달되는 투명한 시스템',
      color: 'text-purple-400',
      bgColor: 'bg-purple-500/10'
    },
    {
      icon: Lock,
      title: '안전한 환경',
      description: 'GPT moderation API로 모든 대화를 모니터링하여 건전한 소통 보장',
      color: 'text-green-400',
      bgColor: 'bg-green-500/10'
    },
    {
      icon: Zap,
      title: '실시간 학습',
      description: '크리에이터의 최신 콘텐츠를 반영하여 항상 최신 상태 유지',
      color: 'text-yellow-400',
      bgColor: 'bg-yellow-500/10'
    },
    {
      icon: BarChart3,
      title: '상세 분석',
      description: '팬들과의 대화 통계와 인사이트로 더 나은 콘텐츠 제작',
      color: 'text-cyan-400',
      bgColor: 'bg-cyan-500/10'
    }
  ];
</script>

<section class="py-20 px-4">
  <div class="max-w-7xl mx-auto">
    <div class="text-center mb-16">
      <h2 class="text-4xl md:text-5xl font-bold mb-4">
        차별화된 <span class="gradient-text">핵심 기능</span>
      </h2>
      <p class="text-xl text-gray-400">다른 플랫폼과는 다른 특별한 경험</p>
    </div>
    
    <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-6">
      {#each features as feature}
        <div class="glass-card p-6 hover:bg-white/10 transition-all duration-300 group">
          <div class="flex items-start gap-4">
            <div class="{feature.bgColor} p-3 rounded-xl group-hover:scale-110 transition-transform">
              <svelte:component this={feature.icon} class="w-6 h-6 {feature.color}" />
            </div>
            <div class="flex-1">
              <h3 class="text-xl font-bold mb-2">{feature.title}</h3>
              <p class="text-gray-400">{feature.description}</p>
            </div>
          </div>
        </div>
      {/each}
    </div>
    
    <!-- Feature highlight -->
    <div class="mt-16 glass-card p-8 bg-gradient-to-br from-primary-500/10 to-secondary-500/10 border-primary-500/20">
      <div class="grid md:grid-cols-2 gap-8 items-center">
        <div>
          <h3 class="text-2xl font-bold mb-4">
            <span class="gradient-text">1:1 맞춤형 AI 캐릭터</span>
          </h3>
          <p class="text-gray-300 mb-4">
            단순한 챗봇이 아닌, 크리에이터의 성격과 말투, 지식을 완벽하게 학습한 진짜 AI 부캐를 만들어드립니다.
          </p>
          <ul class="space-y-2 text-gray-400">
            <li class="flex items-center gap-2">
              <Zap class="w-4 h-4 text-primary-400" />
              크리에이터와의 심층 인터뷰 기반 제작
            </li>
            <li class="flex items-center gap-2">
              <Zap class="w-4 h-4 text-primary-400" />
              콘텐츠 분석을 통한 말투와 성격 학습
            </li>
            <li class="flex items-center gap-2">
              <Zap class="w-4 h-4 text-primary-400" />
              지속적인 업데이트와 개선
            </li>
          </ul>
        </div>
        <div class="relative">
          <div class="absolute inset-0 bg-gradient-to-r from-primary-500 to-secondary-500 blur-3xl opacity-20"></div>
          <div class="relative glass-card p-6 text-center">
            <div class="text-6xl mb-4">🤖</div>
            <div class="text-2xl font-bold gradient-text mb-2">AI 부캐 제작</div>
            <div class="text-gray-400">전문가가 직접 제작하는<br/>프리미엄 서비스</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>