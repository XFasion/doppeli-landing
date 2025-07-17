<script lang="ts">
  import { Users, Heart, TrendingUp, MessageSquare, DollarSign, Clock } from 'lucide-svelte';
</script>

<section class="py-20 px-4">
  <div class="max-w-7xl mx-auto">
    <div class="text-center mb-16">
      <h2 class="text-4xl md:text-5xl font-bold mb-4">
        <span class="gradient-text">양방향 플랫폼</span>으로 모두가 만족
      </h2>
      <p class="text-xl text-gray-400">크리에이터와 팬, 모두에게 가치를 제공합니다</p>
    </div>
    
    <div class="grid md:grid-cols-2 gap-8">
      <!-- Creators -->
      <div class="glass-card p-8 hover:bg-white/10 transition-colors group">
        <div class="flex items-center gap-4 mb-6">
          <div class="w-12 h-12 bg-gradient-to-br from-primary-500 to-primary-600 rounded-xl flex items-center justify-center group-hover:scale-110 transition-transform">
            <Users class="w-6 h-6 text-white" />
          </div>
          <h3 class="text-2xl font-bold">크리에이터를 위한</h3>
        </div>
        
        <ul class="space-y-4">
          <li class="flex items-start gap-3">
            <TrendingUp class="w-5 h-5 text-primary-400 mt-1 flex-shrink-0" />
            <div>
              <div class="font-semibold">24시간 팬 소통</div>
              <div class="text-sm text-gray-400">방송이 없을 때도 팬들과 지속적인 연결</div>
            </div>
          </li>
          <li class="flex items-start gap-3">
            <DollarSign class="w-5 h-5 text-primary-400 mt-1 flex-shrink-0" />
            <div>
              <div class="font-semibold">새로운 수익원</div>
              <div class="text-sm text-gray-400">AI 캐릭터 대화, 선물로 최대 80% 수익 정산</div>
            </div>
          </li>
          <li class="flex items-start gap-3">
            <MessageSquare class="w-5 h-5 text-primary-400 mt-1 flex-shrink-0" />
            <div>
              <div class="font-semibold">브랜드 확장</div>
              <div class="text-sm text-gray-400">AI 부캐로 새로운 콘텐츠와 팬덤 확대</div>
            </div>
          </li>
        </ul>
        
        <div class="mt-8 p-4 bg-primary-500/10 rounded-lg border border-primary-500/20">
          <div class="text-sm text-primary-300">지원 크리에이터</div>
          <div class="text-sm text-gray-400 mt-1">버튜버 • 틱톡커 • 인스타그래머 • 유튜버</div>
        </div>
      </div>
      
      <!-- Fans -->
      <div class="glass-card p-8 hover:bg-white/10 transition-colors group">
        <div class="flex items-center gap-4 mb-6">
          <div class="w-12 h-12 bg-gradient-to-br from-secondary-500 to-secondary-600 rounded-xl flex items-center justify-center group-hover:scale-110 transition-transform">
            <Heart class="w-6 h-6 text-white" />
          </div>
          <h3 class="text-2xl font-bold">팬들을 위한</h3>
        </div>
        
        <ul class="space-y-4">
          <li class="flex items-start gap-3">
            <Clock class="w-5 h-5 text-secondary-400 mt-1 flex-shrink-0" />
            <div>
              <div class="font-semibold">언제든 대화 가능</div>
              <div class="text-sm text-gray-400">좋아하는 크리에이터와 24/7 소통</div>
            </div>
          </li>
          <li class="flex items-start gap-3">
            <Heart class="w-5 h-5 text-secondary-400 mt-1 flex-shrink-0" />
            <div>
              <div class="font-semibold">호감도 시스템</div>
              <div class="text-sm text-gray-400">대화할수록 친밀해지는 특별한 관계</div>
            </div>
          </li>
          <li class="flex items-start gap-3">
            <Users class="w-5 h-5 text-secondary-400 mt-1 flex-shrink-0" />
            <div>
              <div class="font-semibold">크리에이터 지원</div>
              <div class="text-sm text-gray-400">대화와 선물로 직접적인 크리에이터 후원</div>
            </div>
          </li>
        </ul>
        
        <div class="mt-8 p-4 bg-secondary-500/10 rounded-lg border border-secondary-500/20">
          <div class="text-sm text-secondary-300">이용 방법</div>
          <div class="text-sm text-gray-400 mt-1">무료 대화 (하루 5-10회) • 구독으로 무제한 이용</div>
        </div>
      </div>
    </div>
  </div>
</section>