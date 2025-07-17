<script lang="ts">
  import { ArrowRight, Mail, MessageCircle } from 'lucide-svelte';
</script>

<section class="py-20 px-4 relative overflow-hidden">
  <div class="absolute inset-0 bg-gradient-to-t from-primary-900/20 to-transparent"></div>
  
  <div class="max-w-4xl mx-auto relative z-10">
    <div class="glass-card p-12 bg-gradient-to-br from-primary-500/10 to-secondary-500/10 text-center">
      <h2 class="text-4xl md:text-5xl font-bold mb-6">
        지금 바로 <span class="gradient-text">시작하세요</span>
      </h2>
      
      <p class="text-xl text-gray-300 mb-12 max-w-2xl mx-auto">
        크리에이터든 팬이든, AI 캐릭터와 함께하는 새로운 경험이 여러분을 기다립니다.
      </p>
      
      <div class="grid md:grid-cols-2 gap-8 mb-12">
        <!-- For Creators -->
        <div class="glass-card p-8 text-left hover:bg-white/10 transition-colors">
          <h3 class="text-2xl font-bold mb-4">크리에이터이신가요?</h3>
          <p class="text-gray-400 mb-6">
            AI 부캐를 만들어 팬들과 24시간 소통하고 새로운 수익을 창출하세요.
          </p>
          <button class="btn-primary w-full group">
            크리에이터 신청하기
            <ArrowRight class="inline-block w-4 h-4 ml-2 group-hover:translate-x-1 transition-transform" />
          </button>
        </div>
        
        <!-- For Fans -->
        <div class="glass-card p-8 text-left hover:bg-white/10 transition-colors">
          <h3 class="text-2xl font-bold mb-4">팬이신가요?</h3>
          <p class="text-gray-400 mb-6">
            좋아하는 크리에이터의 AI 캐릭터와 특별한 대화를 나눠보세요.
          </p>
          <button class="btn-secondary w-full group">
            캐릭터 둘러보기
            <ArrowRight class="inline-block w-4 h-4 ml-2 group-hover:translate-x-1 transition-transform" />
          </button>
        </div>
      </div>
      
      <!-- Contact Info -->
      <div class="border-t border-gray-800 pt-8">
        <h3 class="text-xl font-bold mb-4">문의하기</h3>
        <div class="flex flex-col sm:flex-row gap-4 justify-center">
          <a href="mailto:support@riply.ai" class="flex items-center gap-2 text-gray-400 hover:text-white transition-colors">
            <Mail class="w-5 h-5" />
            support@riply.ai
          </a>
        </div>
      </div>
    </div>
    
    <!-- Footer -->
    <div class="text-center mt-12 text-gray-500">
      <p>&copy; 2024 스페이스에이아이. All rights reserved.</p>
    </div>
  </div>
</section>