<script lang="ts">
  import { Sparkles, MessageCircle, Heart } from 'lucide-svelte';
  
  export let mounted = false;
</script>

<section class="relative min-h-screen flex items-center justify-center overflow-hidden px-4">
  <!-- Animated Background -->
  <div class="absolute inset-0 bg-gradient-to-br from-primary-900/20 via-transparent to-secondary-900/20 animate-gradient"></div>
  
  <!-- Floating orbs -->
  <div class="absolute inset-0">
    <div class="absolute top-20 left-10 w-72 h-72 bg-primary-500/20 rounded-full blur-3xl animate-float"></div>
    <div class="absolute bottom-20 right-10 w-96 h-96 bg-secondary-500/20 rounded-full blur-3xl animate-float" style="animation-delay: 2s"></div>
    <div class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 w-64 h-64 bg-purple-500/20 rounded-full blur-3xl animate-pulse-slow"></div>
  </div>
  
  <!-- Content -->
  <div class="relative z-10 max-w-7xl mx-auto text-center">
    <div class="mb-8 {mounted ? 'animate-fade-in' : 'opacity-0'}">
      <span class="inline-flex items-center gap-2 px-4 py-2 glass-card rounded-full text-sm">
        <Sparkles class="w-4 h-4 text-primary-400" />
        AI와 함께하는 새로운 팬 소통
      </span>
    </div>
    
    <h1 class="text-5xl md:text-7xl font-bold mb-6 {mounted ? 'animate-fade-in-up' : 'opacity-0'}" style="animation-delay: 0.1s">
      <span class="gradient-text">나만의 AI 부캐</span>를<br/>
      만들어 팔로워들과 소통하세요!
    </h1>
    
    <p class="text-xl md:text-2xl text-gray-400 mb-12 max-w-3xl mx-auto {mounted ? 'animate-fade-in-up' : 'opacity-0'}" style="animation-delay: 0.2s">
      버튜버, 유튜버, 인스타그램 인플루언서를 위한 AI 캐릭터 플랫폼.<br/>
      24시간 팬들과 소통하고 새로운 수익을 창출하세요.
    </p>
    
    <div class="flex flex-col sm:flex-row gap-4 justify-center mb-16 {mounted ? 'animate-fade-in-up' : 'opacity-0'}" style="animation-delay: 0.3s">
      <button class="btn-primary">
        크리에이터로 시작하기
      </button>
      <button class="btn-secondary">
        AI 캐릭터 둘러보기
      </button>
    </div>
    
    <!-- Stats -->
    <div class="grid grid-cols-3 gap-8 max-w-2xl mx-auto {mounted ? 'animate-fade-in' : 'opacity-0'}" style="animation-delay: 0.4s">
      <div class="glass-card p-6">
        <MessageCircle class="w-8 h-8 text-primary-400 mx-auto mb-2" />
        <div class="text-2xl font-bold">24/7</div>
        <div class="text-sm text-gray-400">상시 소통</div>
      </div>
      <div class="glass-card p-6">
        <Heart class="w-8 h-8 text-secondary-400 mx-auto mb-2" />
        <div class="text-2xl font-bold">100%</div>
        <div class="text-sm text-gray-400">팬 만족도</div>
      </div>
      <div class="glass-card p-6">
        <Sparkles class="w-8 h-8 text-purple-400 mx-auto mb-2" />
        <div class="text-2xl font-bold">80%</div>
        <div class="text-sm text-gray-400">수익 정산</div>
      </div>
    </div>
  </div>
  
  <!-- Scroll indicator -->
  <div class="absolute bottom-8 left-1/2 -translate-x-1/2 {mounted ? 'animate-bounce' : 'opacity-0'}">
    <div class="w-6 h-10 glass-card rounded-full p-1">
      <div class="w-1 h-3 bg-white rounded-full mx-auto animate-pulse"></div>
    </div>
  </div>
</section>

<style>
  @keyframes fade-in {
    from {
      opacity: 0;
    }
    to {
      opacity: 1;
    }
  }
  
  @keyframes fade-in-up {
    from {
      opacity: 0;
      transform: translateY(20px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }
  
  .animate-fade-in {
    animation: fade-in 1s ease-out forwards;
  }
  
  .animate-fade-in-up {
    animation: fade-in-up 1s ease-out forwards;
  }
</style>