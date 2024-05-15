<script>
import { ref } from 'vue';
export default {
    setup() {
        const email = ref('');
        const errorMessage = ref('');
        const successMessage = ref('');

        const validateEmail = (email) => {
            const valid = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
            return valid.test(email);
        };

        const subscribe = () => {
            if (!validateEmail(email.value)) {
                errorMessage.value = 'Please enter a valid email address.';
                successMessage.value = '';
            } else {
                errorMessage.value = '';
                successMessage.value = 'Thank You, Your Sign-Up Request Was Successful! Please Check Your Email Inbox To Confirm.';
            }
        };

        return {
            email,
            errorMessage,
            successMessage,
            subscribe
        };
    },
    data() {
        return {
            info: [
                {
                    title: "CONTACT INFO",
                    image: "https://wp.themedemo.org/WP02/WP031/wp-content/uploads/2022/08/footer-location-dot-solid.svg",
                    row1: "2/45 Tower Street,",
                    row2: "New York",
                    row3: "USA",
                    image2: "https://wp.themedemo.org/WP02/WP031/wp-content/uploads/2022/08/footer-phone-solid.svg",
                    row4: "Call Us On 0800",
                    row5: "840 1010",
                    image3: "https://wp.themedemo.org/WP02/WP031/wp-content/uploads/2022/08/footer-envelope-soli.svg",
                    row6: "Demo@Example.Com"
                },
            ],
            information: [
                {
                    row: "Product Support",
                },
                {
                    row: "Checkout",
                },
                {
                    row: "Report Abuse",
                },
                {
                    row: "Redeem Voucher",
                },
                {
                    row: "Order Status",
                },
            ],
            links: [
                {
                    row: "Policies & Rules",
                },
                {
                    row: "Privacy Policy",
                },
                {
                    row: "License Policy",
                },
                {
                    row: "My Account",
                },
                {
                    row: "Locality",
                },
            ],
            newsletter: [
                {
                    row: "Subscribe To Receive",
                },
                {
                    row: "Inspiration,",
                },
                {
                    row: "Ideas & News In Your",
                },
                {
                    row: "Inbox.",
                },
            ],
        }
    },
    methods: {

    }
}
</script>

<template>
    <div class="d-flex justify-content-between text-white container-footer">
        <div v-for="item in info">
            <h6 class="mb-4">{{ item.title }}</h6>
            <div class="d-flex align-items-start gap-3">
                <img decoding="async" class="wp-image-9059" :src="item.image" alt="">
                <p>{{ item.row1 }} <br>
                    {{ item.row2 }} <br>
                    {{ item.row3 }}
                </p>
            </div>
            <div class="d-flex align-items-start gap-3">
                <img decoding="async" class="wp-image-9060" :src="item.image2" alt="">
                <p>{{ item.row4 }} <br>
                    {{ item.row5 }}
                </p>
            </div>
            <div class="d-flex align-items-start gap-3">
                <img decoding="async" class="wp-image-9060" :src="item.image3" alt="">
                <p>{{ item.row6 }}
                </p>
            </div>
        </div>

        <ul>
            <h6 class="mb-4">INFORMATION</h6>
            <li class="lh-lg" v-for="item in information">
                {{ item.row }}
            </li>
        </ul>

        <ul>
            <h6 class="mb-4">USEFUL LINKS</h6>
            <li class="lh-lg" v-for="item in links">
                {{ item.row }}
            </li>
        </ul>

        <div class="d-flex flex-column">
            <ul>
                <h6 class="mb-4">NEWSLETTER</h6>
                <li class="lh-base" v-for="item in newsletter">
                    {{ item.row }}
                </li>
                <div class="d-flex flex-column gap-3 mt-3 max-width">
                    <input v-model="email" class="p-2 bg-dark border-0" type="text" placeholder="Enter Your Email">
                    <button @click="subscribe" class="p-2 border-0">SUBSCRIBE</button>
                    <p v-if="errorMessage" class="text-danger">{{ errorMessage }}</p>
                    <p v-if="successMessage">{{ successMessage }}</p>
                </div>
            </ul>
        </div>
    </div>

</template>

<style scoped lang="scss">
.container-footer {
    padding: 50px;
    background-color: black;

    img {
        width: 15px;
    }

    input[type="text"] {
        color: white;
    }

    .max-width {
        max-width: min-content;
    }
}
</style>