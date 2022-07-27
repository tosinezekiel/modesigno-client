<template>
  <header>
    <div :class="{ 'onScroll': !view.topOfPage}"
      class="hidden lg:grid grid-cols-6 justify-between fixed z-10 w-full py-6 px-44 font-medium"
    >
      <div>
        <div>
          <svg
            width="24"
            height="24"
            viewBox="0 0 24 24"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              d="M4 11H16V13H4V11ZM4 6H20V8H4V6ZM4 18H11.235V16H4V18Z"
              fill="black"
            />
          </svg>
        </div>
        <nuxt-link to="/"> SHOP </nuxt-link>
      </div>
      <div class="col-start-2 col-end-6 justify-self-center">
        <img class="w-36" src="~/assets/images/logo.png" alt="" />
      </div>
      <div>
        <nuxt-link to="/"> ACCOUNT </nuxt-link>
        <div>
          <svg
            width="24"
            height="24"
            viewBox="0 0 24 24"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              d="M3 21L7.486 16.506L3 21ZM5 10.5C5 12.7543 5.89553 14.9163 7.48959 16.5104C9.08365 18.1045 11.2457 19 13.5 19C15.7543 19 17.9163 18.1045 19.5104 16.5104C21.1045 14.9163 22 12.7543 22 10.5C22 8.24566 21.1045 6.08365 19.5104 4.48959C17.9163 2.89553 15.7543 2 13.5 2C11.2457 2 9.08365 2.89553 7.48959 4.48959C5.89553 6.08365 5 8.24566 5 10.5V10.5Z"
              stroke="black"
              stroke-width="2"
              stroke-linecap="round"
            />
          </svg>
        </div>
        <div>
          <svg
            width="36"
            height="36"
            viewBox="0 0 36 36"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              d="M13.33 32C14.5726 32 15.58 30.9926 15.58 29.75C15.58 28.5074 14.5726 27.5 13.33 27.5C12.0874 27.5 11.08 28.5074 11.08 29.75C11.08 30.9926 12.0874 32 13.33 32Z"
              fill="black"
            />
            <path
              d="M27 32C28.2426 32 29.25 30.9926 29.25 29.75C29.25 28.5074 28.2426 27.5 27 27.5C25.7574 27.5 24.75 28.5074 24.75 29.75C24.75 30.9926 25.7574 32 27 32Z"
              fill="black"
            />
            <path
              d="M33.08 5.36999C32.987 5.25527 32.8696 5.1626 32.7365 5.09862C32.6034 5.03465 32.4577 5.00096 32.31 4.99999H11.49L12.14 6.99999H31L28.33 19H13.33L8.76 4.52999C8.71057 4.37645 8.62473 4.23714 8.50981 4.12396C8.39488 4.01077 8.25428 3.92707 8.1 3.87999L4 2.61999C3.87393 2.58125 3.74147 2.56772 3.61017 2.58017C3.47887 2.59262 3.35132 2.63082 3.23478 2.69257C2.99942 2.81728 2.82324 3.03038 2.745 3.28499C2.66676 3.53959 2.69287 3.81486 2.81758 4.05021C2.9423 4.28557 3.1554 4.46175 3.41 4.53999L7 5.63999L11.59 20.14L9.95 21.48L9.82 21.61C9.41434 22.0775 9.1844 22.6718 9.1698 23.2906C9.1552 23.9094 9.35684 24.5139 9.74 25C10.0126 25.3314 10.3589 25.5945 10.7513 25.7682C11.1438 25.9418 11.5714 26.0212 12 26H28.69C28.9552 26 29.2096 25.8946 29.3971 25.7071C29.5846 25.5196 29.69 25.2652 29.69 25C29.69 24.7348 29.5846 24.4804 29.3971 24.2929C29.2096 24.1053 28.9552 24 28.69 24H11.84C11.7249 23.9961 11.6127 23.9625 11.5143 23.9025C11.4159 23.8426 11.3346 23.7583 11.2783 23.6577C11.222 23.5572 11.1926 23.4439 11.1929 23.3286C11.1932 23.2134 11.2232 23.1002 11.28 23L13.69 21H29.13C29.3612 21.0056 29.5871 20.931 29.7695 20.7888C29.9518 20.6466 30.0792 20.4456 30.13 20.22L33.3 6.21999C33.3304 6.0709 33.3264 5.91685 33.2883 5.76955C33.2502 5.62225 33.1789 5.4856 33.08 5.36999Z"
              fill="black"
            />
          </svg>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
    name: "AppHeader",
    data() {
        return {
            view: {
                topOfPage: true
            }
        }
    },
    beforeMount() {
        window.addEventListener('scroll', this.handleScroll)
    },
    methods: {
        handleScroll(){
            if(window.pageYOffset > 0){
                this.view.topOfPage = this.view.topOfPage && false
            } else {
                this.view.topOfPage = !this.view.topOfPage && true
            }
        }
    }
}
</script>

<style scoped>
header > div > div{
  @apply flex
    items-center
    justify-between;
}
.onScroll {
  box-shadow: 0 0 10px #aaa;
  background-color: #fff;
  z-index: 1000;
}
</style>