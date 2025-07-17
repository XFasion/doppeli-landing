<script lang="ts">
  import { UserPlus, MessageSquare, DollarSign, Sparkles } from 'lucide-svelte';
  
  const creatorSteps = [
    {
      icon: UserPlus,
      title: '신청 & 상담',
      description: '간단한 신청서 작성 후 전문가와 1:1 상담'
    },
    {
      icon: Sparkles,
      title: 'AI 캐릭터 제작',
      description: '인터뷰와 콘텐츠 분석을 통한 맞춤형 AI 제작'
    },
    {
      icon: MessageSquare,
      title: '팬들과 소통',
      description: 'AI 캐릭터가 24시간 팬들과 대화'
    },
    {
      icon: DollarSign,
      title: '수익 창출',
      description: '대화, 선물, 구독료의 최대 80% 정산'
    }
  ];
  
  const fanSteps = [
    {
      icon: UserPlus,
      title: '회원가입',
      description: '간단한 가입 후 본인인증'
    },
    {
      icon: Sparkles,
      title: '캐릭터 선택',
      description: '좋아하는 크리에이터의 AI 캐릭터 찾기'
    },
    {
      icon: MessageSquare,
      title: '대화 시작',
      description: '무료로 하루 5-10회 또는 구독으로 무제한'
    },
    {
      icon: DollarSign,
      title: '크리에이터 지원',
      description: '대화와 선물로 크리에이터 직접 후원'
    }
  ];
</script>

<section class="py-20 px-4 relative overflow-hidden">
  <div class="absolute inset-0 bg-gradient-to-t from-purple-900/10 to-transparent"></div>
  
  <div class="max-w-7xl mx-auto relative z-10">
    <div class="text-center mb-16">
      <h2 class="text-4xl md:text-5xl font-bold mb-4">
        <span class="gradient-text">시작하는 방법</span>
      </h2>
      <p class="text-xl text-gray-400">간단한 단계로 시작하세요</p>
    </div>
    
    <div class="grid md:grid-cols-2 gap-12">
      <!-- Creator Process -->
      <div>
        <h3 class="text-2xl font-bold mb-8 text-center">크리에이터</h3>
        <div class="space-y-6">
          {#each creatorSteps as step, index}
            <div class="flex gap-4 group">
              <div class="flex-shrink-0">
                <div class="w-12 h-12 bg-gradient-to-br from-primary-500 to-primary-600 rounded-full flex items-center justify-center text-white font-bold group-hover:scale-110 transition-transform">
                  {index + 1}
                </div>
              </div>
              <div class="flex-1 glass-card p-4 group-hover:bg-white/10 transition-colors">
                <div class="flex items-center gap-2 mb-2">
                  <svelte:component this={step.icon} class="w-5 h-5 text-primary-400" />
                  <h4 class="font-bold">{step.title}</h4>
                </div>
                <p class="text-sm text-gray-400">{step.description}</p>
              </div>
            </div>
            {#if index < creatorSteps.length - 1}
              <div class="ml-6 h-8 border-l-2 border-dashed border-gray-700"></div>
            {/if}
          {/each}
        </div>
      </div>
      
      <!-- Fan Process -->
      <div>
        <h3 class="text-2xl font-bold mb-8 text-center">팬</h3>
        <div class="space-y-6">
          {#each fanSteps as step, index}
            <div class="flex gap-4 group">
              <div class="flex-shrink-0">
                <div class="w-12 h-12 bg-gradient-to-br from-secondary-500 to-secondary-600 rounded-full flex items-center justify-center text-white font-bold group-hover:scale-110 transition-transform">
                  {index + 1}
                </div>
              </div>
              <div class="flex-1 glass-card p-4 group-hover:bg-white/10 transition-colors">
                <div class="flex items-center gap-2 mb-2">
                  <svelte:component this={step.icon} class="w-5 h-5 text-secondary-400" />
                  <h4 class="font-bold">{step.title}</h4>
                </div>
                <p class="text-sm text-gray-400">{step.description}</p>
              </div>
            </div>
            {#if index < fanSteps.length - 1}
              <div class="ml-6 h-8 border-l-2 border-dashed border-gray-700"></div>
            {/if}
          {/each}
        </div>
      </div>
    </div>
  </div>
</section>