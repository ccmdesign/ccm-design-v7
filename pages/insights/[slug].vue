<template>
  <article class="prose">
    <header class="prose__header">
      <center-l class="prose__header-wrapper">
        <hgroup>
          <stack-l>
            <h4 class="brow">This is the brow</h4>
            <h2 class="title">This is the tagline Lorem ipsum dolor sit amet, consectetur adipisicing elit</h2>
            <h3 class="tagline">This is the tagline Lorem ipsum dolor sit amet, consectetur adipisicing elit.
              Reprehenderit excepturi deleniti aut repudiandae ullam perspiciatis</h3>
          </stack-l>
        </hgroup>
        <figure>
          <img
            src="https://images.unsplash.com/photo-1721633617180-97c67428a48e?q=80&w=4140&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
            alt="">
        </figure>
      </center-l>
    </header>
    <section class="main-content">
      <center-l class="prose__wrapper">
        <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. <a href="#">Voluptates facere voluptatem harum
            neque nesciunt</a>
          non repudiandae voluptate reiciendis libero itaque in consequatur aliquid nisi, animi tenetur labore velit
          magnam?
          Voluptate ab ad laudantium illo dolor fuga illum sunt quibusdam. Est omnis corporis aperiam quibusdam suscipit
          voluptatibus debitis reiciendis, ipsam possimus earum beatae. Facilis eos voluptate veritatis unde expedita?
          Ad
          voluptates, ratione rem fugiat laudantium accusantium, nostrum consequatur nesciunt in debitis obcaecati porro
          dolorem repellendus reprehenderit saepe maiores! Quam, vel fuga! Iusto quo, inventore possimus nisi porro
          voluptate molestiae libero asperiores, doloremque accusamus officia laudantium quia alias architecto ipsum
          autem
          incidunt. Veniam, ea quia. Id tenetur aliquam voluptatem eos ipsam quos maiores labore, itaque sint sed
          reiciendis cum nostrum nobis impedit culpa in tempora. Ut odit modi possimus, eligendi quis consequuntur
          assumenda nobis beatae in ea et nulla perspiciatis praesentium molestias laborum, facere aliquid tempore
          similique cupiditate aspernatur accusantium? Suscipit blanditiis non voluptatum autem, magnam cumque dolorum
          quidem a consequuntur natus vel quisquam numquam repellat fugiat sequi, perferendis modi officia. Doloremque
          recusandae suscipit reprehenderit, minus totam sit laborum id repellat voluptate vero quisquam, magnam
          asperiores porro quos temporibus facere veniam perspiciatis beatae. Architecto omnis inventore ratione
          consectetur dolorum assumenda sunt ea officia voluptatibus nihil autem provident labore sequi qui odio,
          laborum
          porro. Sint maiores dolorem, ipsum quisquam quis veritatis.</p>
        <h3>This is an intermetiate title</h3>
        <ul>
          <li>Lorem ipsum dolor sit amet consectetur adipisicing elit.</li>
          <li>Lorem ipsum dolor sit amet consectetur adipisicing elit.</li>
          <li>Lorem ipsum dolor sit amet consectetur adipisicing elit.</li>
          <li>Lorem ipsum dolor sit amet consectetur adipisicing elit.</li>
        </ul>

        <h4>This is an intermetiate title</h4>
        <ol>
          <li>Lorem ipsum dolor sit amet consectetur adipisicing elit.</li>
          <li>Lorem ipsum dolor sit amet consectetur adipisicing elit.</li>
          <li>Lorem ipsum dolor sit amet consectetur adipisicing elit.</li>
          <li>Lorem ipsum dolor sit amet consectetur adipisicing elit.</li>
        </ol>

        <h5>This is an intermetiate title</h5>
        <p>Hic, natus placeat doloribus nobis quod nulla, unde
          recusandae, soluta at possimus expedita vitae maxime laborum labore nemo! Reiciendis necessitatibus repellat
          quas quod explicabo similique veritatis tempora voluptatibus temporibus! Quasi quibusdam et animi perferendis
          atque sit saepe, amet tenetur modi qui, est voluptatibus rem minus dolores eaque harum nostrum laborum earum
          deserunt architecto temporibus aliquam commodi fugiat. Laudantium nemo illum repudiandae maiores quia dolores
          voluptatibus corrupti consequuntur consequatur perspiciatis aliquid aut maxime, saepe ipsam reprehenderit
          aperiam hic distinctio laborum dolorum, vero quasi eaque! Quod omnis ea nobis quam error? Minima quas numquam
          tempore voluptatum officia ipsum qui suscipit assumenda nobis tenetur provident iusto nulla itaque earum harum
          maiores, dolor minus labore dignissimos sequi! Fuga porro similique veritatis, ut enim quam fugit blanditiis,
          laudantium, doloribus mollitia consequatur nisi pariatur recusandae alias ad quia fugiat est nihil voluptates
          architecto aperiam vero molestiae! Magni, voluptatibus.</p>
        <h6>This is an intermetiate title</h6>
        <p>Hic, natus placeat doloribus nobis quod nulla, unde
          recusandae, soluta at possimus expedita vitae maxime laborum labore nemo! Reiciendis necessitatibus repellat
          quas quod explicabo similique veritatis tempora voluptatibus temporibus! Quasi quibusdam et animi perferendis
          atque sit saepe, amet tenetur modi qui, est voluptatibus rem minus dolores eaque harum nostrum laborum earum
          deserunt architecto temporibus aliquam commodi fugiat. Laudantium nemo illum repudiandae maiores quia dolores
          voluptatibus corrupti consequuntur consequatur perspiciatis aliquid aut maxime, saepe ipsam reprehenderit
          aperiam hic distinctio laborum dolorum, vero quasi eaque! Quod omnis ea nobis quam error? Minima quas numquam
          tempore voluptatum officia ipsum qui suscipit assumenda nobis tenetur provident iusto nulla itaque earum harum
          maiores, dolor minus labore dignissimos sequi! Fuga porro similique veritatis, ut enim quam fugit blanditiis,
          laudantium, doloribus mollitia consequatur nisi pariatur recusandae alias ad quia fugiat est nihil voluptates
          architecto aperiam vero molestiae! Magni, voluptatibus.</p>
      </center-l>
    </section>
  </article>

</template>

<script setup>
    const route = useRoute()

    const postData = await queryContent('articles').where({
        slug: route.params.slug
    }).findOne();

    const data = reactive({
        post: postData,
    });
</script>

<style lang="scss" scoped>
// basic layout
.prose__header {
  height: auto;
}

.prose__header hgroup {
  display: flex;
  flex-direction: column;
  justify-content: center;
  min-height: min(800px, 60svh);
}

// Making the header wider than the actual content. 
.prose__header-wrapper { max-width: min(160ch, 100cqi); }

// Limiting the width of the content to 80ch. Best for readability.
.prose__wrapper { max-width: min(80ch, 100cqi); }

// header styles
.prose__header {
  text-align: center;
}

.brow {
  font-size: clamp(.85rem, 2.5vw, 1.25rem);
  font-weight: bold;
  text-transform: uppercase;
  font-family: var(--body-font);
  color: var(--accent-color);
}

.title {
  margin-top: var(--s-1);
  color: var(--primary-color);
  font-size: clamp(1.5rem, 5vw, 3.5rem);
  line-height: clamp(115%, 2vw, 150%);

  @media screen and (max-width: 768px) { font-weight: 200; }
}

.tagline {
  font-size: clamp(.85rem, 3vw, 1.5rem);
  font-weight: 300;
  line-height: 1.35;
  margin-top: var(--s1);
  color: var(--primary-color);
}

.prose__header figure {
  margin-block: var(--s3);
  box-shadow: 0 0 64px  hsla(var(--base-hsl), .15);
}


.main-content {
  ul, ol {
      *+* { margin-top: var(--s-1); }
    }
}

.main-content {
  --space: var(--s1);
  --prose-vertical-space: var(--s0);
  --prose-caption-font-style: italic;
  --prose-figure-vertical-space: var(--s2);
  --prose-gap: var(--base-gap);
  --heading-color: var(--accent-color);
}

.main-content * + * {
  margin-top: var(--prose-vertical-space);
}


.main-content {
  h3, h4, h5, h6 { 
    margin-top: var(--s2); 
    margin-bottom: 0;
  }


  h3 {
    font-size: 1.5rem;
    color: var(--base-color);
    font-weight: 400;
  }

  h4 {
    font-size: 1.25rem;
    font-weight: 600;
    color: var(--accent-color);
  }
  
  h5, h6 {
    font-weight: 600;
    font-size: 1rem;
  }

  h5 { 
    color: var(--base-color); 
    text-transform: uppercase;
  }
  h6 { color: var(--base-color); }

  p {
    font-weight: 300;
    line-height: 2;
  }

  blockquote {
    font-size: 1.4em;
    border-left: 4px solid var(--accent-color);
    padding-left: var(--s1);
    font-style: italic;
  }

  cite {
    font-style: italic;
    font-size: 1rem;
  }
}
// /* Font Size for Headings */
// h1 ~ .brow {
//   font-size: 1.5em;
// }

// h2 ~ .brow {
//   font-size: 1.15em;
// }

// h3 ~ .brow {
//   font-size: 1em;
// }

// h4 ~ .brow {
//   font-size: .8em;
// }

// h5 ~ .brow {
//   font-size: .6em;
// }


/* Spacing for headings */
h2 {
  margin-top: var(--s1);
}

h3 {
  margin-top: var(--s1);
}

h4 {
  margin-top: var(--s1);
}

h5 {
  margin-top: var(--s1);
}




.brow,
/* Spacing for .brow */
figure,
/* Spacing for figure */
blockquote,
/* Spacing for blockquote */
blockquote + *,
/* Spacing for blockquote */
hr,
/* Spacing for other horizontal ruler */
hr + * {
  margin-top: var(--s2);
}

figure {
  img { border-radius: 16px; }
}

/* Colors */
h2 {
  --heading-color: var(--primary-color);
}

h3 {
  --heading-color: var(--primary-color);
}

h4 {
  --heading-color: var(--primary-color);
}

h5 {
  --heading-color: var(--primary-color);
}


a {
  color: var(--accent-color);
  text-decoration: underline;
}

// h2 {
//   font-size: 3rem;
//   font-weight: 100;
//   line-height: .9;
// }

// h4 {
//   font-weight: bold;
//   text-transform: uppercase;
//   font-family: var(--body-font);
// }

// h3 {
//   font-weight: 400;
//   line-height: 1.2;
//   font-family: var(--body-font);
// }
</style>
