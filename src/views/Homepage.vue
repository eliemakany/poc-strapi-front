<template>
    <div>
        <Header v-bind:content="content"></Header>
        <PageBuilder v-bind:contents="pagesComponents"></PageBuilder>
    </div>
</template>

<script>
import axios from 'axios'
import Header from '@/components/Header.vue'
import PageBuilder from "../components/PageBuilder";

export default {
    name : 'Homepage',
    components: {
      PageBuilder,
        Header
    },

    data: function(){
        return {
            content: {},
            pagesComponents: []
        }
    },

    created: function() {
        axios({
            url: 'http://localhost:1337/graphql',
            method: 'post',
            data: {
                query: `
                query {
                  homepage {
                    title
                    baseline
                    ctaText
                    ctaLink
                    metadonnees {
                      Metatitle
                      Metadescription
                      AliasUrl
                      CanonicalUrl
                    },
                    content {
                      __typename
                      ... on ComponentTexte2Colonnes {
                        title2Col
                        baseline
                        blocTextLeft
                        blocTextRight
                      }
                      ... on ComponentTexte3Colonnes {
                        title3Col
                        baseline
                        blocTextLeft
                        blockTextMiddle
                        blockTextRight
                      }
                    }
                  }
                }
               `
            }
        }).then((result) => {
            this.content = result.data.data.homepage;
            this.pagesComponents = this.content.content;
        });
    }
}
</script>

<style scoped>

</style>>