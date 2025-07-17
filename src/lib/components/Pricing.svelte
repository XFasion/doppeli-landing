<script lang="ts">
  import { Check, TrendingUp, Crown } from 'lucide-svelte';
  
  const pricingPlans = [
    {
      name: '무료 체험',
      price: '0',
      description: '캐릭터와의 첫 만남',
      features: [
        '하루 5-10회 대화',
        '기본 캐릭터 기능',
        '텍스트 대화만 가능',
        '커뮤니티 접근'
      ],
      cta: '무료로 시작',
      popular: false,
      icon: Check
    },
    {
      name: '스탠다드',
      price: '9,900',
      description: '팬들에게 가장 인기!',
      features: [
        '무제한 대화',
        '음성 대화 지원',
        '호감도 시스템 전체 이용',
        '특별 이벤트 참여',
        '선물 기능 이용'
      ],
      cta: '구독 시작하기',
      popular: true,
      icon: TrendingUp
    },
    {
      name: '프리미엄',
      price: '19,900',
      description: '최고의 팬 경험',
      features: [
        '스탠다드의 모든 기능',
        '1:1 특별 대화 모드',
        '독점 콘텐츠 접근',
        '크리에이터 직접 소통 기회',
        '우선 응답 서비스'
      ],
      cta: 'VIP 되기',
      popular: false,
      icon: Crown
    }
  ];
</script>

<section class="py-20 px-4">
  <div class="max-w-7xl mx-auto">
    <div class="text-center mb-16">
      <h2 class="text-4xl md:text-5xl font-bold mb-4">
        합리적인 <span class="gradient-text">요금제</span>
      </h2>
      <p class="text-xl text-gray-400">크리에이터가 직접 설정하는 구독료</p>
    </div>
    
    <div class="grid md:grid-cols-3 gap-8 mb-16">
      {#each pricingPlans as plan}
        <div class="relative {plan.popular ? 'scale-105' : ''}">
          {#if plan.popular}
            <div class="absolute -top-4 left-1/2 -translate-x-1/2 z-10">
              <span class="px-4 py-1 bg-gradient-to-r from-primary-500 to-secondary-500 text-white text-sm font-bold rounded-full">
                BEST CHOICE
              </span>
            </div>
          {/if}
          
          <div class="glass-card p-8 h-full flex flex-col {plan.popular ? 'border-primary-500/50' : ''} hover:bg-white/10 transition-colors">
            <div class="text-center mb-6">
              <div class="w-12 h-12 mx-auto mb-4 bg-gradient-to-br {plan.popular ? 'from-primary-500 to-secondary-500' : 'from-gray-600 to-gray-700'} rounded-xl flex items-center justify-center">
                <svelte:component this={plan.icon} class="w-6 h-6 text-white" />
              </div>
              <h3 class="text-2xl font-bold mb-2">{plan.name}</h3>
              <p class="text-gray-400 text-sm mb-4">{plan.description}</p>
              <div class="text-4xl font-bold">
                {#if plan.price === '0'}
                  무료
                {:else}
                  ₩{plan.price}<span class="text-lg text-gray-400">/월</span>
                {/if}
              </div>
            </div>
            
            <ul class="space-y-3 mb-8 flex-1">
              {#each plan.features as feature}
                <li class="flex items-start gap-2">
                  <Check class="w-5 h-5 text-green-400 mt-0.5 flex-shrink-0" />
                  <span class="text-gray-300">{feature}</span>
                </li>
              {/each}
            </ul>
            
            <button class="{plan.popular ? 'btn-primary' : 'btn-secondary'} w-full">
              {plan.cta}
            </button>
          </div>
        </div>
      {/each}
    </div>
    
    <!-- Revenue Share Info -->
    <div class="glass-card p-8 text-center">
      <h3 class="text-2xl font-bold mb-4">크리에이터 수익 정산</h3>
      <div class="grid md:grid-cols-3 gap-8">
        <div>
          <div class="text-4xl font-bold gradient-text">70%</div>
          <div class="text-gray-400">일반 크리에이터</div>
        </div>
        <div>
          <div class="text-4xl font-bold gradient-text">80%</div>
          <div class="text-gray-400">파트너 크리에이터</div>
        </div>
        <div>
          <div class="text-4xl font-bold gradient-text">100%</div>
          <div class="text-gray-400">투명한 정산</div>
        </div>
      </div>
      <p class="text-gray-400 mt-6">
        모든 수익(구독료, 선물, 후원)은 실시간으로 집계되며, 월 단위로 정산됩니다.
      </p>
    </div>
  </div>
</section>