<template>
  <svg viewBox="0 0 45 45" xmlns="http://www.w3.org/2000/svg">
    <g filter="url(#filter0_d_2_1392)">
      <path
        d="M31.8104 27.7966C31.1033 28.5037 30.3726 28.8572 29.6184 28.8572C28.8405 28.8337 28.0981 28.4683 27.391 27.7612L22.6533 23.0236L18.0218 27.6551C17.3383 28.3387 16.6312 28.6922 15.9005 28.7158C15.1934 28.7158 14.4981 28.374 13.8145 27.6905C13.131 27.007 12.7892 26.3116 12.7892 25.6045C12.8128 24.8739 13.1663 24.1668 13.8499 23.4832L18.4814 18.8517L13.9206 14.2908C13.2135 13.5837 12.8599 12.853 12.8599 12.0988C12.8599 11.3446 13.2253 10.6021 13.9559 9.87141C14.663 9.16431 15.3819 8.82254 16.1126 8.84611C16.8669 8.84611 17.5975 9.19966 18.3046 9.90677L22.8655 14.4676L27.497 9.83606C28.1806 9.15252 28.8759 8.81075 29.583 8.81075C30.3137 8.78718 31.0208 9.11717 31.7043 9.8007C32.3879 10.4842 32.7178 11.1913 32.6943 11.922C32.6943 12.6291 32.3525 13.3245 31.669 14.008L27.0374 18.6395L31.775 23.3772C32.4821 24.0843 32.8475 24.8267 32.871 25.6045C32.8946 26.3352 32.5411 27.0659 31.8104 27.7966Z"
      />
    </g>
    <defs>
      <filter
        id="filter0_d_2_1392"
        x="0.975677"
        y="0.961868"
        width="43.7796"
        height="43.7796"
        filterUnits="userSpaceOnUse"
        color-interpolation-filters="sRGB"
      >
        <feFlood flood-opacity="0" result="BackgroundImageFix" />
        <feColorMatrix
          in="SourceAlpha"
          type="matrix"
          values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0"
          result="hardAlpha"
        />
        <feOffset dy="4" />
        <feGaussianBlur stdDeviation="2" />
        <feComposite in2="hardAlpha" operator="out" />
        <feColorMatrix
          type="matrix"
          values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.25 0"
        />
        <feBlend
          mode="normal"
          in2="BackgroundImageFix"
          result="effect1_dropShadow_2_1392"
        />
        <feBlend
          mode="normal"
          in="SourceGraphic"
          in2="effect1_dropShadow_2_1392"
          result="shape"
        />
      </filter>
    </defs>
  </svg>
</template>

<script>
export default {
  name: "ExitIcon",
};
</script>

<style scoped>
svg {
  display: block;
  width: 30px;
  height: 30px;
}

@media (max-width: 639px) {
  svg {
    width: 24px;
    height: 24px;
  }
}
</style>