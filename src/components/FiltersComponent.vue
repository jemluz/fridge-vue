<template>
    <div class="filters">
        <p>Filtros</p>

        <div class="plus_minus">

          <button class="filter_button minus_button" @click="applyConsumedFilter()">
            <svg class="minus_icon" width="14" height="3" viewBox="0 0 14 3" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M13 0H1C0.734784 0 0.48043 0.105356 0.292893 0.292892C0.105357 0.480429 0 0.734784 0 1L0 2C0 2.26522 0.105357 2.51957 0.292893 2.70711C0.48043 2.89464 0.734784 3 1 3H13C13.2652 3 13.5196 2.89464 13.7071 2.70711C13.8946 2.51957 14 2.26522 14 2V1C14 0.734784 13.8946 0.480429 13.7071 0.292892C13.5196 0.105356 13.2652 0 13 0Z"/>
            </svg>
          </button>

          <button class="filter_button plus_button" @click="applyReplacementFilter()">
            <svg class="plus_icon" width="15" height="15" viewBox="0 0 15 15" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M13.501 6.00098H9.00098V1.50098C9.00098 1.23576 8.89562 0.981405 8.70808 0.793869C8.52055 0.606333 8.26619 0.500977 8.00098 0.500977H7.00098C6.73576 0.500977 6.48141 0.606333 6.29387 0.793869C6.10633 0.981405 6.00098 1.23576 6.00098 1.50098V6.00098H1.50098C1.23576 6.00098 0.981406 6.10633 0.79387 6.29387C0.606333 6.48141 0.500977 6.73576 0.500977 7.00098L0.500977 8.00098C0.500977 8.26619 0.606333 8.52055 0.79387 8.70808C0.981406 8.89562 1.23576 9.00098 1.50098 9.00098H6.00098V13.501C6.00098 13.7662 6.10633 14.0205 6.29387 14.2081C6.48141 14.3956 6.73576 14.501 7.00098 14.501H8.00098C8.26619 14.501 8.52055 14.3956 8.70808 14.2081C8.89562 14.0205 9.00098 13.7662 9.00098 13.501V9.00098H13.501C13.7662 9.00098 14.0205 8.89562 14.2081 8.70808C14.3956 8.52055 14.501 8.26619 14.501 8.00098V7.00098C14.501 6.73576 14.3956 6.48141 14.2081 6.29387C14.0205 6.10633 13.7662 6.00098 13.501 6.00098Z"/>
            </svg>
          </button>

        </div>
      </div>
</template>

<script>
export default {
    name: 'FiltersComponent',
    methods: {
        applyConsumedFilter() {
            console.log('Filtro de consumo ativado')
        },
        applyReplacementFilter() {
            console.log('Filtro de reposição ativado')
        }
    }
}
</script>

<style lang="scss" scopped>
    .filters {
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        align-items: center;
        margin: 18px 115px 0px 118px;

        .plus_minus {
            display: flex;
            flex-direction: row;

            .filter_button {
                justify-content: space-between;
                height: 33px;
                width: 33px;
                border: 0px;
                border-radius: 10px;
                margin-left: 12px;
                display: flex;
                align-items: center;
                justify-content: center;
            }

            .minus_button {
                background-color: #FEECEC80;
                transition: all .3s ease-in;

                &:hover {
                    background-color: #FEECEC;

                    .minus_icon {
                        fill: #EF7A7A;
                    }
                }

                .minus_icon {
                    fill: #EF7A7A80;
                    transition: all .3s ease-in;
                }
            }

            .plus_button{
                background-color: #E1F9F480;
                transition: all .3s ease-in;

                &:hover {
                    background-color: #E1F9F4;

                    .plus_icon{
                        fill: #33AFAA;
                    }
                }

                .plus_icon {
                    fill: #33AFAA80;
                    transition: all .3s ease-in;
                }
            }

        }

    }
</style>
