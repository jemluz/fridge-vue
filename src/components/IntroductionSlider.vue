<template>
    <div class="introduction">
        <h4>{{ title }}</h4>
        <p>{{ subtitle }}</p>

        <nav class="slider_nav">
            <button @click="changeToContentOne(true)">
                <svg class="left_icon" viewBox="0 0 23 32" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path d="M20 29.5L3 17L20 3" stroke-width="5" stroke-linecap="round" stroke-linejoin="round"/>
                </svg>
            </button>

            <span class="default_index" v-bind:class="{ active_index: isOne }"></span>
            <span class="default_index" v-bind:class="{ active_index: !isOne }"></span>

            <button @click="changeToContentOne(false)">
                <svg class="right_icon" viewBox="0 0 23 32" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path d="M3 3L20 15.5L3 29.5" stroke-width="5" stroke-linecap="round" stroke-linejoin="round"/>
                </svg>
            </button>
        </nav>
    </div>
</template>

<script>
export default {
    name: 'IntroductionSlider',
    data: () => {
        return {
            isOne: true,
            title: '',
            subtitle: '',
        }
    },
    methods: {
        changeToContentOne(boolean) {
            this.isOne = boolean;

            if(this.isOne) {
                this.title = 'Monitore suas comidas';
                this.subtitle = 'Saiba sempre o que há na sua geladeira';
            } else {
                this.title = 'Entenda o seu consumo';
                this.subtitle = 'Você vai descobrir quais são os recursos mais usados por você.';
            }
        },
    },
    beforeMount() {
        this.changeToContentOne(true);
    }
}
</script>

<style lang="scss" scoped>
    .introduction {
        // margin-top: 23px;
        margin-bottom: 12px;
        display: flex;
        flex-direction: column;
        justify-content: center;

        h4 {
            font-size: 16px;
        }

        p {
            font-size: 14px;
            color: #8D8D8D;
            height: 45px;
            width: 272px;
        }

        .slider_nav{
            display: flex;
            align-items: center;
            width: 100px;
            margin: 16px auto;
            justify-content: center;

            button {
                background-color: transparent;
                border: none;
                margin: 0px 8px;
            }

            .left_icon,
            .right_icon {
                width: 8px;
                stroke: #cbcbcb;
            }

            .default_index {
                background-color: transparent;
                border: 2px solid #cbcbcb;
                border-radius: 50%;
                height: 6px;
                width: 6px;
                transition: all .3s ease-in;
                margin: 0px 6px;
            }

            .active_index {
                background-color: #33AFAA;
                border: 2px solid #33AFAA;
                border-radius: 50%;
                height: 6px;
                width: 6px;
                margin: 0px 6px;
            }
        }

    }
</style>