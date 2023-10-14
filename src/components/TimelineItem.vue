<script setup lang="ts">
import { TimelinePost } from '../posts';
import { DateTime } from 'luxon';

defineProps<{
    post: TimelinePost;
}>()
</script>

<template>
    <a class="panel-block is-flex is-flex-direction-column is-align-items-flex-start">
        <a>{{ post.title }}</a>
        <div>{{ post.created?.toLocaleString(DateTime.DATE_FULL) }}</div>
    </a>
</template>