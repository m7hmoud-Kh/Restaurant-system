<!-- eslint-disable prettier/prettier -->
<template>
    <div class="container">
        <form class="col-md-6 m-auto" @submit.prevent="SubmitSignUp">
            <h2>Sign UP</h2>
            <div class="form-group">
                <input type="text" placeholder="Type Your Name" class="form-control" v-model="name" />
            </div>
            <br />
            <div class="form-group">
                <input type="email" placeholder="Type Your Email" class="form-control" v-model="email" />
            </div>
            <br />

            <div class="form-group">
                <input type="password" placeholder="Type Your Password" class="form-control" v-model="password" />
            </div>
            <br />

            <div class="form-group">
                <button type="submit" class="btn btn-primary">Sign Up Now</button>
            </div>
        </form>
    </div>
</template>

<script>
import { reactive, toRefs } from "vue";
export default {
    name: "SignUpComponent",
    setup() {
        const credentails = reactive({
            name: "",
            email: "",
            password: "",
        });



        return {
            ...toRefs(credentails),
        };
    },
};
</script>
