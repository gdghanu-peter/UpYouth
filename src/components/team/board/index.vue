<template>
  <div class="mb-16 mx-4">
    <div class="flex flex-col items-center justify-center gap-2 md:gap-4">
      <h1 class="text-primary-700 mb-3 sm:mb-6 text-3xl sm:text-5xl font-bold">Executive Board</h1>
      <p class="mb-8 text-center text-base  sm:text-xl max-w-[700px]">
        UpYouth leadership team consists of talented and ambitious young people, who share a deep passion for startups.
      </p>
    </div>
    <div>
        <UCarousel
            :items="executiveBoard"
            v-slot="{ item }"
            :ui="{
              item: 'basis-full justify-center',
              indicators: {
                active: 'bg-primary-700',
                inactive: 'bg-gray-300',
                wrapper:
                  'absolute flex items-center justify-center gap-3 -bottom-10 inset-x-0'
              }
            }"
            indicators
          >
            <TeamBoardItem :item="item"></TeamBoardItem>
          </UCarousel>
    </div>
  </div>
</template>

<script setup lang="ts">
import type { ExecutiveBoardItem } from '~/types/board'

const executiveBoard = ref<ExecutiveBoardItem[]>([
  {
    name: 'Dao Phan Anh',
    img: '/team/dao-phan-anh.png',
    title: 'President',
    content: [
      `Phan Anh can spend the whole day discussing with you about investing and building, as he believes in the virtuous cycle connecting these two factors.`,
      `His investment journey spans from seed-stage ventures at LvlUp Ventures to working on Vietnam's largest renewables M&A deal; managing a $2 million student-run public equity portfolio, to investments for a $4.5 billion foundation.`,
      `He is also a real builder, shown by how he played a pivotal role in scaling a solar financing startup and builded TechYouth Incubator 2023. Now he is leading UpYouth Tech Startup Ecosystem, using his experience to connect with and bridge the gap between investors and startup builders.`,
      `Outside of work, he enjoys boxing as school's club captain, listening to Ted Seides' Capital Allocators and Lenny's Podcast, and binging comedy-drama (most recently Succession).`
    ]
  },
  {
    name: 'Nguyen Canh Huy',
    img: '/team/nguyen-canh-huy.png',
    title: 'Community & Partership Director',
    content: [
      `As a Computer Science student, Canh Huy discovered his passion for entrepreneurship after working at Got It AI Vietnam, an AI-driven startup based in Silicon Valley.`,
      `He began his journey at UpYouth as a Growth Associate and quickly advanced to the role of Director of External Partnerships, developing his proficiency in strategic analysis and systemic thinking. Those skillset has made him a competent player, both in the industry and academic sectors.`,
      `He got a chance to work professionally at KPMG, VinFast, and Viettel Software. At the same time, Huy made it to the final round of Cornell EMI Corning Case Competition 2024, just months after becoming the First Runner-up at the ICAEW Mainland China and South-East Asia Business Competition 2024.`,
      `Out of office, he is such a player. Karaoke, games, trips, you barely see him miss the party! You can only know how crazy he is after working with him. Cheers!`
    ]
  },
  {
    name: 'Pham Van Luong',
    img: '/team/pham-van-luong.png',
    title: 'Growth Director',
    content: [
      `Luong Pham is indeed an explorer, who is ready to wear different hats to develop her diverse background knowledge.`,
      `Before becoming the Director of Growth, she spent over 2 years in the Startup Knowledge Department, delving into the realm of product building and transforming business concepts into reality.`,
      `Now switching to the Growth playground, she once again combines her corporate finance expertise as a Financial Planning Analyst at Starbucks with hands-on experience working on growth strategies at GIMO, a YC W'22 startup.`,
      `Her broad understanding of both the corporate and startup ecosystems under multiple roles has made her a formiddable asset to our team.`,
      `Beside work, Luong is a perennial fan of Hong Kong movies, and is obsessed with Wong Kar-wai's Chungking Express. Don't be surprised if you catch her raving for hours about Takeshi Kaneshiro's eyes at Bottom Up Club to a random stranger.`
    ]
  }
])
</script>
