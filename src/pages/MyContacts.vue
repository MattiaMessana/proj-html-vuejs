<script>
export default {
    data() {
        return {
            contactUs: [
                {
                    icon: "http://www.w3.org/2000/svg",
                    title: "ADDRESS INFO",
                    info: [
                        {
                            row1: "502 New Design Str, Melbourne,",
                            row2: "San Francisco, CA 94110,",
                            row3: "United States of America​ Australia",
                        }
                    ]
                },
                {
                    icon: "",
                    title: "CONTACT INFO",
                    info: [
                        {
                            row1: "068 26589 996",
                            row2: "demo@example.com",
                        }
                    ]
                },
                {
                    icon: "",
                    title: "WORKING HOURS",
                    info: [
                        {
                            row1: "Open: 8:00AM – Close: 18:00PM",
                            row2: "Saturday – Sunday: Close",
                        }
                    ]
                },
            ]
        };
    },
    methods: {
        // getIconUrl(iconName) {
        //     return new URL(`../assets/${iconName}`, import.meta.url).href;
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
                <div class="d-flex flex-column">
                    <svg data-name="Layer 1" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 631.8 980">
                        <path
                            d="M517,852.9a22.24,22.24,0,0,1-34,0c-12.2-14.6-298.9-358.8-298.9-527.1C184.2,151.7,325.8,10,500,10S815.9,151.7,815.9,325.8C815.8,494.1,529.2,838.3,517,852.9ZM500,54.3c-149.7,0-271.5,121.8-271.5,271.5,0,130.5,209.6,400.8,271.5,477.8,61.9-77,271.6-347.3,271.6-477.8C771.5,176.1,649.7,54.3,500,54.3Zm4.2,377.9c-72.3,0-131.1-58.8-131.1-131A131.23,131.23,0,0,1,504.2,170.1c72.2,0,131,58.8,131,131.1S576.4,432.2,504.2,432.2Zm0-217.8a86.75,86.75,0,1,0,86.7,86.8A86.85,86.85,0,0,0,504.2,214.4ZM353.6,749.7a22.17,22.17,0,0,1,8.6,43.5c-87.8,17.3-133.7,48.3-133.7,69.9,0,33.7,105.8,82.6,271.5,82.6s271.6-48.9,271.6-82.6c0-21.3-45.1-52-131.2-69.4a22.14,22.14,0,1,1,8.8-43.4c105.9,21.4,166.7,62.6,166.7,112.8C815.8,946.4,656.9,990,500,990S184.2,946.4,184.2,863.1C184.2,812.3,245.9,771,353.6,749.7Z"
                            transform="translate(-184.1 -10)"></path>
                    </svg>
                    <svg data-name="Layer 1" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 979.92 972.7">
                        <path
                            d="M723.5,986.3c-62.6,0-143.4-41.8-200.2-76.9-76-47-158-112-230.7-183l-.3-.3L269.2,703C198.3,630.1,133.5,548,86.7,471.8,51.7,415,10,333.9,10,271.2c0-67.2,47.9-138.4,68.5-166,16.1-21.5,72.2-91.6,119.9-91.6,19.6,0,40.7,12.9,68.4,41.7,24.5,25.5,48.1,57.2,63.5,79.3,20.7,29.7,39.9,60.7,54,87.4,22.8,43.3,25.4,61.8,25.4,72,0,20.6-10.7,38.4-31.9,53-13.9,9.6-30.6,16.9-46.8,23.9-10.9,4.7-28.3,12.3-34.9,17.6,2.3,9.8,12.4,33.6,39.8,73.8,25.5,37.5,58.5,78.2,88.2,108.8,30.6,29.8,71.1,62.9,108.6,88.4,40.1,27.4,63.8,37.6,73.7,39.9,5.3-6.7,12.8-24.1,17.5-35,7-16.2,14.2-33,23.8-46.9,14.6-21.2,32.4-31.9,52.9-31.9,10.2,0,28.7,2.6,71.9,25.5,26.7,14.1,57.7,33.3,87.2,54.1,22,15.5,53.7,39,79.1,63.6,28.8,27.8,41.6,49,41.6,68.6,0,47.8-69.9,104.1-91.4,120.2-27.4,20.7-98.5,68.7-165.5,68.7ZM332.7,685.5c69.8,68.1,148.1,130.3,220.6,175.1,70.3,43.4,132.3,68.3,170.2,68.3,33.7,0,81.7-20.6,128.5-55.2,20.5-15.2,39.2-32,52.5-47.5,12.6-14.5,17.1-24,18.3-27.8-4.9-10.4-33.7-43.1-100.9-89.6-26.4-18.2-53.7-35-76.8-47.2-29.1-15.3-41.2-18-43.9-18.4-1.1.7-4.2,3.4-9.1,11.5-5.4,9.1-10.6,21.1-15.6,32.7-6.2,14.3-12.5,29.1-20.4,41-12.7,19.4-28.3,29.2-46.4,29.2h-1c-8.8-.2-35.6-.8-108.3-50.4-40.1-27.4-83.7-62.9-116.6-95.1l-.5-.5c-32-32.9-67.5-76.6-94.8-116.8-49.5-72.9-50.1-99.7-50.3-108.5-.4-18.4,9.3-34.4,28.9-47.3,11.9-7.9,26.8-14.4,41.2-20.6,11.6-5,23.5-10.2,32.6-15.6,8.1-4.8,10.7-8,11.5-9.1-.4-2.8-3.1-14.9-18.3-44.1-12.2-23.2-28.9-50.5-47.1-77-46.4-67.4-79-96.3-89.4-101.2-3.8,1.2-13.3,5.8-27.8,18.4-15.4,13.4-32.3,32.1-47.4,52.7-34.5,46.9-55,95-55,128.8,0,37.9,24.8,100.1,68.2,170.5C180.3,514.5,242.3,593,310.3,662.9l22.4,22.6ZM673.8,479.4A21.08,21.08,0,0,1,653.1,462c-5.1-29.2-22-54.6-47.5-71.5-25.9-17.1-57.5-23.5-89-17.9a21.07,21.07,0,0,1-7.3-41.5c42.2-7.5,84.6,1.1,119.5,24.2,35.2,23.3,58.6,58.6,65.8,99.3a21,21,0,0,1-17,24.4,17.56,17.56,0,0,1-3.8.4Zm126.4-54.3a21.08,21.08,0,0,1-20.7-17.4c-10-56.7-42.7-105.9-92-138.5-49.7-32.9-110.4-45.1-171-34.4a21.07,21.07,0,0,1-7.3-41.5c71.1-12.6,142.7,1.9,201.4,40.8,59.1,39.1,98.3,98.2,110.2,166.4a21,21,0,0,1-17,24.4c-1.2.1-2.4.2-3.6.2ZM969,409.4A21.08,21.08,0,0,1,948.3,392c-17-96.7-72.7-180.7-156.9-236.3C706.9,99.7,603.8,78.9,501,97.1a21.07,21.07,0,0,1-7.3-41.5c113.3-20,227.3,3,320.8,64.9,93.9,62.1,156.1,155.9,175.1,264.2a21.08,21.08,0,0,1-17,24.4,21.86,21.86,0,0,1-3.6.3Z"
                            transform="translate(-10 -13.6)"></path>
                    </svg>
                    <svg data-name="Layer 1" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 990 990">
                        <path
                            d="M956.1,307.33A496.59,496.59,0,1,0,995,500,493.55,493.55,0,0,0,956.1,307.33ZM500,945.8c-245.81,0-445.8-200-445.8-445.8S254.19,54.2,500,54.2s445.8,200,445.8,445.8S745.81,945.8,500,945.8Z"
                            transform="translate(-5 -5)"></path>
                        <polygon
                            points="519.6 98 470.4 98 470.4 508.18 720.68 675.03 748.04 634.12 519.6 481.82 519.6 98">
                        </polygon>
                    </svg>
                </div>
                <div class="d-flex flex-column">
                    <ul v-for="item in contactUs">
                        <h5>{{ item.title }}</h5>
                        <li v-for="info in item.info" :key="info.row1">
                            {{ info.row1 }}
                        </li>
                        <li v-for="info in item.info" :key="info.row2">
                            {{ info.row2 }}
                        </li>
                        <li v-for="info in item.info" :key="info.row3">
                            {{ info.row3 }}
                        </li>
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