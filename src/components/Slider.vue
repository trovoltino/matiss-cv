<template>
    <div class="slider">
        <div class="left-field">
            <div class="left-text">
                <h2>Dont Have An Account?</h2>
                <div class="underline"></div>
            </div>
            <div class="left-text">
                <p>Lorem ipsum dolor sit amet,
                    consectetur adipiscing elit. 
                    Suspendisse lacinia odio auctor.
                </p>
            </div>
            <div class="left-text">
                <div class="left"><button id="btn-signup-move" class="btn-login-left" type="button">sign up</button></div>
            </div>
        </div>
        <div class="right-field">
            <div class="left-text">
                <h2>Have An Account?</h2>
                <div class="underline"></div>
            </div>
            <div class="left-text">
                <p>Lorem ipsum dolor sit amet,
                    consectetur adipiscing elit. 
                </p>
            </div>
            <div class="left-text">
                <div class="left"><button id="btn-login-move" class="btn-login-left" type="button">Login</button></div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
  name: 'Slider',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.slider {
    position: absolute;
    left: 50%;
    top: 50%;
    transform: translate(-50%,-50%)
}
</style>
