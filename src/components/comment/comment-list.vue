<template>
    <div class='clist'>
        <comment v-for='c in comments'
                 :comment='c'
                 :key='c.id'
                 @deletes='doDelete'>
        </comment>
    </div>
</template>

<script>
 import commentItem from './comment-item';

 export default {
     props: ['comments'],
     methods: {
         doDelete(id) {
             this.$emit('deletes', id);
         }
     },
     components: {
         comment: commentItem
     }
 };
</script>
