<script setup lang="ts">
import { links, donate, jobs } from '@/components/data/links'
import ProfilePicture from '@/components/ProfilePicture.vue'
import LinkBtn from '@/components/LinkBtn.vue'
import Separator from '@/components/SeparatorLine.vue'
import FooterIcons from '@/components/FooterIcons.vue'
</script>

<template>
  <div class="flex flex-col items-center gap-y-6">
    <ProfilePicture class="mt-8" />
    <h1 class="font-bold text-xl text-center uppercase">david barrero</h1>
    <FooterIcons />
    <Separator />
    <LinkBtn
      v-for="item in jobs"
      :key="item.title"
      :title="item.title"
      :link="item.link"
      :alt="item.alt"
    ></LinkBtn>
    <Separator />
    <LinkBtn
      v-for="item in links"
      :key="item.title"
      :title="item.title"
      :link="item.link"
      :alt="item.alt"
    ></LinkBtn>
    <Separator />
    <LinkBtn
      :title="donate.title"
      :link="donate.link"
      :alt="donate.alt"
    ></LinkBtn>
  </div>
</template>
