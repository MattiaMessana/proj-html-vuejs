<script>
export default {
    data() {
        return {
            // imageName: "fotografia.webp"
        };
    },
    methods: {
        // getImagePath(img) {
        //     return new URL(`/src/assets/img/${img}`, import.meta.url).href;
        // }
    },
};
</script>

<template>
    <!-- hero -->
    <div class="bg-image">
        <div class="contacts">
            <h2>CONTACTS</h2>
            <div class="home-contacts">
                <router-link class="home" :to="{ name: 'home' }">Home</router-link>
                <span> / Contacts</span>
            </div>
        </div>
        <!-- <img :src="getImagePath(imageName)"> -->
    </div>

    <!-- google maps -->
    <div class="container-maps">
        <div class="maps"></div>
    </div>

    <!-- validation -->
    <form class="row needs-validation container-validation" novalidate>
        <div class="">
            <label for="validationCustom01" class="form-label">Your name</label>
            <input type="text" class="form-control rounded-0 bg-color border-0" id="validationCustom01" value=""
                required>
            <div class="valid-feedback">
                Looks good!
            </div>
        </div>

        <div class="">
            <label for="validationCustom03" class="form-label">Your email</label>
            <input type="text" class="form-control rounded-0 bg-color border-0" id="validationCustom03" required>
            <div class="invalid-feedback">
                Please provide a valid email.
            </div>
        </div>

        <div class="">
            <label for="validationCustom05" class="form-label">Subject</label>
            <input type="text" class="form-control rounded-0 bg-color border-0" required>
            <div class="invalid-feedback">
                Please provide a valid subject.
            </div>
        </div>

        <div class="form-floating">
            <div class="comments">
                <label for="floatingTextarea">Comments</label>
            </div>
            <textarea class="form-control rounded-0 bg-color border-0" placeholder="Leave a comment here"
                id="floatingTextarea"></textarea>
        </div>

        <div class="">
            <button class="btn btn-dark rounded-0 btn-width" type="submit">SUBMIT</button>
        </div>
    </form>
</template>

<style scoped lang="scss">
@use "../style/variables" as *;

.bg-image {
    background-image: url(/src/assets/img/bredcum-img.jpg);
    background-size: cover;
    background-position: center;

    .contacts {
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        padding: 100px;

        h2 {
            color: white;
            font-size: 3rem;
        }

        .home-contacts {
            color: white;

            .home {
                color: white;
            }
        }
    }
}

.container-maps {
    display: flex;
    justify-content: center;
    padding-top: 50px;

    .maps {
        height: 300px;
        width: 90%;
        border: 1px solid black;
    }
}

.container-validation {
    border: 1px solid lightgray;
    width: 50%;
    margin: 30px;
    gap: 30px;
    padding: 30px;

    .bg-color {
        background-color: $lightgray;
    }

    .comments {
        padding-bottom: 10px;
    }

    .btn-width {
        width: 100%;
    }
}
</style>