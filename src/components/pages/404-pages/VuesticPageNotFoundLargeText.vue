<template>
  <div class="vuestic-page-not-found-large-text">
    <div class="vuestic-page-not-found-large-text__content">
      <div class="vuestic-page-not-found-large-text__wallpaper">
        <router-link class="i-vuestic vuestic-page-not-found-large-text__i-vuestic" :to="{path: '/'}"/>
      </div>
      <div class="vuestic-page-not-found-large-text__wallpaper">
        <h1 class="vuestic-page-not-found-large-text__number">404</h1>
      </div>
      <div class="vuestic-page-not-found-large-text__wallpaper">
        <h3 class="vuestic-page-not-found-large-text__text">The page's gone fishing.</h3>
      </div>
      <div class="vuestic-page-not-found-large-text__wallpaper col-md-12">
        <div class="row vuestic-page-not-found-large-text__message">
          <h4 class="vuestic-page-not-found-large-text__text-small">If you feel that it's not right, please send us a message at &nbsp</h4>
          <a href="mailto:hello@epicmax.co">hi@epicmax.co</a>
        </div>
      </div>
      <div class="vuestic-page-not-found-large-text__wallpaper-button col-md-12">
        <router-link :to="{ path: './dashboard' }">
          <button class="btn btn-primary">
            {{'Back to dashboard'}}
          </button>
        </router-link>
      </div>
    </div>
    <div class="vuestic-page-not-found-large-text__not-found-wallpaper-sad">
      <img src="https://i.imgur.com/hu80UGU.png" class="vuestic-page-not-found-large-text__sad-image"/>
    </div>
    <made-by-component/>
  </div>
</template>

<script>
import MadeByComponent from './MadyByComponent'

export default {
  name: 'vuestic-page-not-found-large-text',
  components: {
    MadeByComponent
  }
}
</script>

<style lang="scss">
.vuestic-page-not-found-large-text {
  height: 100vh;
  background-color: $top-nav-bg;

  &__number {
    font-size: 250px;
    text-align: center;
    color: white;
  }

  &__sad-image {
    width: 505px;
    height: 400px;
    bottom: 0;
  }

  &__text {
    padding-top: 3%;
    color: white;
  }

  &__text-small {
    font-size: 16px;
    line-height: 1.5;
    text-align: center;
    color: white;
    font-weight: normal;
  }

  &__i-vuestic {
    margin-top: 3%;
  }

  &__not-found-wallpaper-sad {
    position: absolute;
    overflow: hidden;
    height: 40%;
    width: 100%;
    bottom: 0;
    padding-left: 80%;
  }

  &__wallpaper {
    background-color: $top-nav-bg;
    overflow: hidden;
    display: flex;
    align-items: flex-start;
    justify-content: center;
  }

  &__wallpaper-button {
    min-height: 150px;
    width: 340px;
    background-color: $top-nav-bg;
    overflow: hidden;
    display: flex;
    margin-left: 43%;
    align-items: flex-start;
    justify-content: center;
  }

  &__i-vuestic {
    z-index: 2;
    height: $auth-wallpaper-ivuestic-h;
    width: 100%;
  }

  @include media-breakpoint-down(xs) {
    .vuestic-page-not-found-large-text {
      height: $auth-mobile-main-h;

      &__sad-image {
        width: 360px;
        height: 300px;
        padding-left: 100px;
        bottom: 0;
      }

      &__wallpaper-button {
        width: 100%;
        margin-left: 0;
      }

      &__number {
        font-size: 150px;
      }

      &__message {
        justify-content: center;
      }

      &__i-vuestic {
        margin-top: 5%;
      }

      &__not-found-wallpaper-sad {
        padding: 0;
        height: 36%;
      }

      &__text-small {
        font-size: 15px;
      }
    }
  }
}
</style>
