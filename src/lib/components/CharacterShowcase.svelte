<script lang="ts">
  import { Heart, MessageCircle, Sparkles } from 'lucide-svelte';
  
  const characters = [
    {
      name: '루나',
      creator: '@moonlight_vtuber',
      type: '버튜버',
      avatar: 'https://api.dicebear.com/7.x/avataaars/svg?seed=luna&backgroundColor=c084fc',
      likes: '12.5K',
      messages: '45.2K',
      status: 'online',
      gradient: 'from-purple-500 to-pink-500'
    },
    {
      name: '서연',
      creator: '@seoyeon_daily',
      type: '틱톡커',
      avatar: 'https://api.dicebear.com/7.x/avataaars/svg?seed=seoyeon&backgroundColor=f472b6',
      likes: '8.7K',
      messages: '32.1K',
      status: 'online',
      gradient: 'from-pink-500 to-rose-500'
    },
    {
      name: '지우',
      creator: '@jiwoo_insta',
      type: '인스타그래머',
      avatar: 'https://api.dicebear.com/7.x/avataaars/svg?seed=jiwoo&backgroundColor=60a5fa',
      likes: '15.3K',
      messages: '58.9K',
      status: 'busy',
      gradient: 'from-blue-500 to-cyan-500'
    },
    {
      name: '하늘',
      creator: '@sky_streamer',
      type: '스트리머',
      avatar: 'https://api.dicebear.com/7.x/avataaars/svg?seed=sky&backgroundColor=34d399',
      likes: '9.9K',
      messages: '38.7K',
      status: 'online',
      gradient: 'from-green-500 to-emerald-500'
    }
  ];
</script>

<section class="py-20 px-4 relative overflow-hidden">
  <div class="absolute inset-0 bg-gradient-to-b from-transparent via-purple-900/10 to-transparent"></div>
  
  <div class="max-w-7xl mx-auto relative z-10">
    <div class="text-center mb-16">
      <h2 class="text-4xl md:text-5xl font-bold mb-4">
        인기 <span class="gradient-text">AI 캐릭터</span>들
      </h2>
      <p class="text-xl text-gray-400">지금 바로 대화를 시작해보세요</p>
    </div>
    
    <div class="grid md:grid-cols-2 lg:grid-cols-4 gap-6">
      {#each characters as character}
        <div class="glass-card p-6 hover:bg-white/10 transition-all duration-300 group cursor-pointer">
          <!-- Status indicator -->
          <div class="flex justify-between items-start mb-4">
            <div class="flex items-center gap-2">
              <div class="w-2 h-2 rounded-full {character.status === 'online' ? 'bg-green-400' : 'bg-yellow-400'} animate-pulse"></div>
              <span class="text-xs text-gray-400">
                {character.status === 'online' ? '대화 가능' : '바쁨'}
              </span>
            </div>
            <span class="text-xs glass-card px-2 py-1 rounded-full">{character.type}</span>
          </div>
          
          <!-- Avatar -->
          <div class="relative mb-4">
            <div class="w-24 h-24 mx-auto rounded-full overflow-hidden bg-gradient-to-br {character.gradient} p-1 group-hover:scale-110 transition-transform">
              <img src={character.avatar} alt={character.name} class="w-full h-full rounded-full bg-white" />
            </div>
            <div class="absolute -bottom-2 -right-2 w-8 h-8 bg-gradient-to-br {character.gradient} rounded-full flex items-center justify-center">
              <Sparkles class="w-4 h-4 text-white" />
            </div>
          </div>
          
          <!-- Info -->
          <div class="text-center mb-4">
            <h3 class="text-xl font-bold mb-1">{character.name}</h3>
            <p class="text-sm text-gray-400">{character.creator}</p>
          </div>
          
          <!-- Stats -->
          <div class="flex justify-around mb-4">
            <div class="text-center">
              <div class="flex items-center gap-1 text-pink-400">
                <Heart class="w-4 h-4" />
                <span class="text-sm font-semibold">{character.likes}</span>
              </div>
              <div class="text-xs text-gray-500">좋아요</div>
            </div>
            <div class="text-center">
              <div class="flex items-center gap-1 text-blue-400">
                <MessageCircle class="w-4 h-4" />
                <span class="text-sm font-semibold">{character.messages}</span>
              </div>
              <div class="text-xs text-gray-500">대화</div>
            </div>
          </div>
          
          <!-- CTA -->
          <button class="w-full py-2 bg-gradient-to-r {character.gradient} text-white text-sm font-semibold rounded-lg hover:opacity-90 transition-opacity">
            대화 시작하기
          </button>
        </div>
      {/each}
    </div>
    
    <div class="text-center mt-12">
      <button class="btn-secondary">
        더 많은 캐릭터 보기
      </button>
    </div>
  </div>
</section>