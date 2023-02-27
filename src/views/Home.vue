<template>
  <section class="[ homepage ][ flex ]">
    <div class="[ homepage__banner ]" />
    <article class="[ homepage__infos ]">
      <div class="[ info ][ flex ]" data-type="column">
        <h3 class="[ label ][ caption font-primary ]">PERFUME</h3>
        <h2 class="[ title ][ font-secondary ]">
          Gabrielle Essence Eau De Parfim
        </h2>

        <p class="[ caption font-primary ]">
          A floral, solar and voluptuous interpretation composed by Oliver
          Polge, Perfumer-Creator for the House of CHANEL
        </p>

        <div class="[ price ][ flex ]">
          <span class="[ font-secondary ]"> $149.99 </span>
          <span class="[ font-primary ]"> $169.99 </span>
        </div>

        <button class="[ font-primary ][ flex ]"><svg width="15" height="16" xmlns="http://www.w3.org/2000/svg"><path d="M14.383 10.388a2.397 2.397 0 0 0-1.518-2.222l1.494-5.593a.8.8 0 0 0-.144-.695.8.8 0 0 0-.631-.28H2.637L2.373.591A.8.8 0 0 0 1.598 0H0v1.598h.983l1.982 7.4a.8.8 0 0 0 .799.59h8.222a.8.8 0 0 1 0 1.599H1.598a.8.8 0 1 0 0 1.598h.943a2.397 2.397 0 1 0 4.507 0h1.885a2.397 2.397 0 1 0 4.331-.376 2.397 2.397 0 0 0 1.12-2.021ZM11.26 7.99H4.395L3.068 3.196h9.477L11.26 7.991Zm-6.465 6.392a.8.8 0 1 1 0-1.598.8.8 0 0 1 0 1.598Zm6.393 0a.8.8 0 1 1 0-1.598.8.8 0 0 1 0 1.598Z" fill="#FFF"/></svg>Add to Cart</button>
      </div>
    </article>
  </section>
</template>

<script>
export default {
  name: "HomeView",
};
</script>

<style lang="scss">
.homepage {
  --radius-border: 11px;
  height: 100%;
  font-size: 14px;

  &__banner {
    width: 50%;
    background-image: url("./imgs/image-product-desktop.jpg");
    background-size: cover;

    border-top-left-radius: var(--radius-border);
    border-bottom-left-radius: var(--radius-border);
  }

  &__infos {
    background-color: var(--white);
    height: 100%;
    width: 50%;

    border-top-right-radius: var(--radius-border);
    border-bottom-right-radius: var(--radius-border);
    .info {
      padding: 24px;
      gap: 24px;
      .label {
        letter-spacing: 7px;
      }
      .title {
        font-size: 32px;
      }
      .price {
        gap: 12px;
        & > span:first-child {
          font-size: 32px;
          color: var(--dark-cyan);
        }
        & > span:nth-child(2) {
          color: var(--grayish-blue);
          text-decoration: line-through;
          margin-top: 4px;
        }
      }
      & > button {
        border: none;
        border-radius: var(--radius-border);
        background-color: var(--dark-cyan);
        color: var(--white);

        height: 45px;
        font-weight: 700;
        justify-content: center;
        align-items: center;
        gap: 10px;
        transition: 0.3s all ease;

        &:hover {
          background-color: var(--dark-blue);
          cursor: pointer;
        }
      }
    }
  }
}
@media only screen and (max-width: 428px){
  .homepage {
    flex-direction: column;
    height: auto;

    &__banner {
      width: 100%;
      height: 200px;
      border-bottom-left-radius: 0;
      border-bottom-right-radius: 0;
      border-top-right-radius: var(--radius-border);
      background-image: url("./imgs/image-product-mobile.jpg");
      background-size: cover;
    }

    &__infos {
      width: 91%;
      border-top-left-radius: 0;
      border-top-right-radius: 0;
      border-bottom-left-radius: var(--radius-border);
      padding: 16px;
      .info {
        gap: 16px;
        .label {
          letter-spacing: 3px;
        }
        .title {
          font-size: 24px;
        }
        .price {
          flex-direction: column;
          & > span:first-child {
            font-size: 24px;
          }
          & > span:nth-child(2) {
            margin-top: 8px;
          }
        }
        & > button {
          height: 40px;
          font-size: 14px;
        }
      }
    }
  }
}

</style> 