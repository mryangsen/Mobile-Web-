<template>
    <div class="article-detail-main">
        这是明细id为: {{$route.params.id}}
        <button @click="$router.go(-1);">返回</button>
    </div>
</template>
<script>
export default {
    name: 'ArticleDetail'
}
</script>

