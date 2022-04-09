<template>
    <div class="transaction">
        <div class="info_time">
            <div class="hour">
                <svg class= "svg_transaction clock_icon" width="21" height="22" viewBox="0 0 21 22" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path d="M10.5 0.548309C8.46464 0.548507 6.47508 1.15223 4.78287 2.28314C3.09065 3.41405 1.77178 5.02136 0.993034 6.90181C0.214286 8.78226 0.0106328 10.8514 0.407826 12.8476C0.80502 14.8438 1.78522 16.6774 3.22448 18.1165C4.66375 19.5556 6.49743 20.5356 8.49366 20.9326C10.4899 21.3296 12.559 21.1258 14.4394 20.3469C16.3198 19.5679 17.9269 18.2489 19.0577 16.5566C20.1884 14.8643 20.792 12.8746 20.792 10.8393C20.7896 8.11053 19.7045 5.4942 17.7748 3.56475C15.8452 1.6353 13.2288 0.550428 10.5 0.548309V0.548309ZM15.394 16.1623C15.3144 16.242 15.2198 16.3053 15.1158 16.3485C15.0117 16.3916 14.9001 16.4138 14.7875 16.4138C14.6748 16.4138 14.5632 16.3916 14.4592 16.3485C14.3551 16.3053 14.2606 16.242 14.181 16.1623L9.89397 11.8743C9.81425 11.7948 9.75104 11.7004 9.70796 11.5964C9.66489 11.4924 9.6428 11.3809 9.64297 11.2683V5.69431C9.65056 5.47195 9.74423 5.26124 9.90421 5.10663C10.0642 4.95202 10.278 4.8656 10.5005 4.8656C10.7229 4.8656 10.9367 4.95202 11.0967 5.10663C11.2567 5.26124 11.3504 5.47195 11.358 5.69431V10.9133L15.395 14.9483C15.4747 15.0279 15.538 15.1224 15.5811 15.2265C15.6243 15.3306 15.6465 15.4421 15.6465 15.5548C15.6465 15.6675 15.6243 15.779 15.5811 15.8831C15.538 15.9872 15.4747 16.0817 15.395 16.1613L15.394 16.1623Z" />
                </svg>
                <p>{{ getTime() }}</p>
            </div>
            <div class="date">
                <svg class= "svg_transaction calendar_icon" width="11" height="12" viewBox="0 0 11 12" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path d="M0.749023 10.526C0.749023 10.8087 0.861334 11.0798 1.06125 11.2797C1.26116 11.4796 1.5323 11.592 1.81502 11.592H9.63102C9.91374 11.592 10.1849 11.4796 10.3848 11.2797C10.5847 11.0798 10.697 10.8087 10.697 10.526V4.48895H0.749023V10.526ZM2.17002 6.26595C2.17029 6.17188 2.20777 6.08174 2.27429 6.01522C2.34081 5.9487 2.43095 5.91122 2.52502 5.91095H4.65702C4.75109 5.91122 4.84124 5.9487 4.90775 6.01522C4.97427 6.08174 5.01176 6.17188 5.01202 6.26595V8.39695C5.01176 8.49102 4.97427 8.58117 4.90775 8.64768C4.84124 8.7142 4.75109 8.75169 4.65702 8.75195H2.52502C2.43095 8.75169 2.34081 8.7142 2.27429 8.64768C2.20777 8.58117 2.17029 8.49102 2.17002 8.39695V6.26595ZM9.63102 1.64695H8.56502V0.580952C8.56476 0.486881 8.52727 0.396739 8.46075 0.330221C8.39424 0.263702 8.30409 0.226216 8.21002 0.225952L7.49902 0.225952C7.40495 0.226216 7.31481 0.263702 7.24829 0.330221C7.18177 0.396739 7.14429 0.486881 7.14402 0.580952V1.64695H4.30202V0.580952C4.30176 0.487226 4.26455 0.397383 4.19846 0.330922C4.13238 0.26446 4.04275 0.226742 3.94902 0.225952L3.23602 0.225952C3.14195 0.226216 3.05181 0.263702 2.98529 0.330221C2.91877 0.396739 2.88129 0.486881 2.88102 0.580952V1.64695H1.81502C1.5323 1.64695 1.26116 1.75926 1.06125 1.95918C0.861334 2.15909 0.749023 2.43023 0.749023 2.71295L0.749023 3.77895H10.697V2.71295C10.697 2.43023 10.5847 2.15909 10.3848 1.95918C10.1849 1.75926 9.91374 1.64695 9.63102 1.64695Z" />
                </svg>
                <p>{{ getDate() }}</p>
            </div>
        </div>
        <div class="info_transaction">
            <h4>{{ transactionObject.name }}</h4>
            <div class=" transaction_type type_down">
                <svg class= "svg_transaction arrow_icon arrow_down" width="7" height="13" viewBox="0 0 7 13" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path d="M4.40716 8.70303V0.432026C4.40716 0.345287 4.37291 0.262057 4.31186 0.200443C4.2508 0.138829 4.16789 0.103818 4.08116 0.103027H2.54816C2.50495 0.103027 2.46217 0.111537 2.42225 0.128071C2.38234 0.144605 2.34607 0.16884 2.31552 0.19939C2.28497 0.229941 2.26073 0.26621 2.2442 0.306126C2.22767 0.346042 2.21916 0.388821 2.21916 0.432026V8.70303H0.958156C0.828088 8.70286 0.700896 8.7413 0.592695 8.81348C0.484493 8.88566 0.40015 8.98833 0.350353 9.10849C0.300555 9.22864 0.287543 9.36088 0.312965 9.48844C0.338387 9.616 0.401098 9.73314 0.493156 9.82503L2.84915 12.181C2.97236 12.3042 3.13944 12.3734 3.31366 12.3734C3.48787 12.3734 3.65495 12.3042 3.77816 12.181L6.13415 9.82503C6.22621 9.73314 6.28893 9.616 6.31435 9.48844C6.33977 9.36088 6.32676 9.22864 6.27696 9.10849C6.22716 8.98833 6.14282 8.88566 6.03462 8.81348C5.92641 8.7413 5.79922 8.70286 5.66915 8.70303H4.40716Z" />
                </svg>
                <h4>{{ transactionObject.quantity }} unidades</h4>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'ItemComponent',
    props: ['transactionObject'],
    methods: {
        getTime() {
            let dateTime = new Date(this.transactionObject.dateTime);
            const hours = dateTime.getHours() < 10 ? `0${(dateTime.getHours() - 3)}` : (dateTime.getHours() - 3);
            const minutes = dateTime.getMinutes() < 10 ? `0${dateTime.getMinutes()}` : dateTime.getMinutes();
            return `${hours}:${minutes}`;
        },
        getDate() {
            let dateTime = new Date(this.transactionObject.dateTime);
            const day = dateTime.getDay() < 10 ? `0${dateTime.getDay()}` : dateTime.getDay();
            const month = dateTime.getMonth() < 10 ? `0${dateTime.getMonth()}` : dateTime.getMonth();
            console.log(new Date(null, null, null, 0, 30).toJSON())
            return `${day}/${month}/${dateTime.getFullYear()}`;
        }
    },
}
</script>

<style lang="scss" scoped>
    .transaction {
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        padding: 18px 0px;
        border-bottom: 1px solid #EAF3F1;

        .info_time {
            display: flex;
            flex-direction: column;

            .hour {
                display: flex;
                flex-direction: row;
                align-items: center;
                margin-bottom: 12px;
                margin-top: 6px;
            }

            .date {
                display: flex;
                flex-direction: row;
                align-items: center;
            }

            .hour,
            .date {
                p {
                    margin-left: 12px;
                    color: #B8B8B8;
                    font-size: 12px;
                }
            }

            .clock_icon,
            .calendar_icon {
                fill: #B8B8B8;
            }
        }

        .info_transaction {
            display: flex;
            flex-direction: column;
            align-items: flex-end;

            h4 {
                font-size: .8rem;
            }

            .transaction_type {
                display: flex;
                flex-direction: row;
                justify-content: space-between;
                align-items: center;
                padding: 6px 12px;
                border-radius: 8px;
                margin-top: 6px;

                h4 {
                    margin-left: 12px;
                    font-size: .6rem;
                }
            }

            .type_up {
                background-color: #33AFAA10;

                h4 {
                    color: #33AFAA;
                }

                .arrow_up {
                    fill: #33AFAA;
                }
            }

            .type_down {
                background-color: #EF7A7A10;

                h4 {
                    color: #EF7A7A;
                }

                .arrow_down {
                    fill: #EF7A7A;
                }
            }
        }

        .svg_transaction {
            width: 12px;
            height: 12px;
        }

    }
</style>