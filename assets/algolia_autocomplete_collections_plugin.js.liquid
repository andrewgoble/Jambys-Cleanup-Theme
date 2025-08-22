(async function(algolia) {
  'use strict';

  const getAlgoliaResults = algolia.externals.getAlgoliaResults;
  const { config, translations, headerTemplate, collectionsTemplate } = algolia;

  const index_suffix = await config.index_suffix;

  algolia.collectionsPlugin = {
    getSources({ query }) {
      return [
        {
          sourceId: 'collections',
          getItems() {
            return getAlgoliaResults({
              searchClient: algolia.searchClient,
              queries: [
                {
                  indexName: config.index_prefix + 'collections' + index_suffix,
                  query,
                  params: {
                    hitsPerPage: config.collections_autocomplete_hits_per_page,
                    clickAnalytics: config.analytics_enabled
                  },
                },
              ],
              transformResponse({ hits }) {   
                const results = hits[0].filter(hit => {
                  return hit.handle == "womens" || 
                  hit.handle == "jambys" ||
                  hit.handle == "long-jambys" ||
                  hit.handle == "new-arrivals" ||
                  hit.handle == "sleepwear" ||
                  hit.handle == "mens" || 
                  hit.handle == "bottoms" || 
                  hit.handle == "tops" ||
                  hit.handle == "sale-collection" || 
                  hit.handle == "fall-bestsellers" || 
                  hit.handle == "chilluxe" ||  
                  hit.handle == "best-gifts" || 
                  hit.handle == "limited-stock-left" ||
                  hit.handle == "best-sellers"
                });
                return results
              },
            });
          },
          templates: {
            header({ html, state }) {
              const resource = translations.collections;
              return headerTemplate({ html, state }, resource);
            },
            item({ item, html, components }) {
              const itemLink = `${window.Shopify.routes.root}collections/${item.handle}`;
              return collectionsTemplate({ item, html, components }, itemLink);
            },
          },
        }
      ];
    },
  }
})(window.algoliaShopify);