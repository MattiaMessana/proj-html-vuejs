<script>
export default {
    data() {
        return {

        };
    },
    methods: {

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
    </div>

    <!-- google maps -->
    <div class="container-maps">
        <div class="maps"></div>
    </div>

    <div class="d-flex cont-valid-us">
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

        <!-- contact us -->
        <div class="contact-us">
            <h1>CONTACT US</h1>
            <div class="d-flex align-items-start mt-4">
                <svg data-name="Layer 1" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 631.8 980">
                    <path
                        d="M517,852.9a22.24,22.24,0,0,1-34,0c-12.2-14.6-298.9-358.8-298.9-527.1C184.2,151.7,325.8,10,500,10S815.9,151.7,815.9,325.8C815.8,494.1,529.2,838.3,517,852.9ZM500,54.3c-149.7,0-271.5,121.8-271.5,271.5,0,130.5,209.6,400.8,271.5,477.8,61.9-77,271.6-347.3,271.6-477.8C771.5,176.1,649.7,54.3,500,54.3Zm4.2,377.9c-72.3,0-131.1-58.8-131.1-131A131.23,131.23,0,0,1,504.2,170.1c72.2,0,131,58.8,131,131.1S576.4,432.2,504.2,432.2Zm0-217.8a86.75,86.75,0,1,0,86.7,86.8A86.85,86.85,0,0,0,504.2,214.4ZM353.6,749.7a22.17,22.17,0,0,1,8.6,43.5c-87.8,17.3-133.7,48.3-133.7,69.9,0,33.7,105.8,82.6,271.5,82.6s271.6-48.9,271.6-82.6c0-21.3-45.1-52-131.2-69.4a22.14,22.14,0,1,1,8.8-43.4c105.9,21.4,166.7,62.6,166.7,112.8C815.8,946.4,656.9,990,500,990S184.2,946.4,184.2,863.1C184.2,812.3,245.9,771,353.6,749.7Z"
                        transform="translate(-184.1 -10)"></path>
                </svg>
                <div class="d-flex flex-column align-items-center">
                    <ul>
                        <h5>ADDRESS INFO</h5>
                        <li>502 New Design Str, Melbourne,</li>
                        <li>San Francisco, CA 94110,</li>
                        <li>United States of America​ Australia</li>
                    </ul>
                </div>
            </div>
        </div>
    </div>
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

.cont-valid-us {
    width: 90%;
    margin-right: auto;
    margin-left: auto;

    .container-validation {
        border: 1px solid lightgray;
        width: 50%;
        margin: 50px 50px 0 0;
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

    .contact-us {
        margin-top: 50px;
        width: 50%;

        svg {
            width: 20px;
        }
    }
}
</style>