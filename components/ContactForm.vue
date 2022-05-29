<template>
  <article class="contact-form content-container">
    <aside>
      <div class="aside__info">
        <h3 class="mark">Let's Talk</h3>
        <p>
          Feel free to get in touch with me, I am always open to new ideas or
          opportunities to be part of your vision.
        </p>
        <p>
          If you have any questions, business propositions; just write me a
          message
        </p>
      </div>
      <Socials class="aside__social" />
    </aside>
    <form action="">
      <div class="form-group">
        <label for="name">Full Name:</label>
        <input
          id="name"
          type="text"
          name="name"
          required
          placeholder="Enter Your Full Name"
          class="form-control"
        />
      </div>
      <div class="form-group">
        <label for="email">Email Address:</label>
        <input
          id="email"
          type="email"
          name="email"
          required
          placeholder="username@example.com"
          class="form-control"
        />
      </div>
      <div class="form-group">
        <label for="phone">Phone Number: <small>(Optional)</small></label>
        <input
          id="phone"
          type="text"
          name="phone"
          placeholder="+254000000000"
          class="form-control"
          maxlength="13"
        />
      </div>
      <div class="form-group">
        <label for="message">Message:</label>
        <textarea
          id="message"
          name="message"
          cols="30"
          rows="10"
          class="form-control"
        ></textarea>
      </div>
      <div class="form-group">
        <button type="submit" class="primary-btn submit-btn">
          Send Message
        </button>
      </div>
    </form>
  </article>
</template>

<script>
export default {
  name: 'ContactForm',
}
</script>

<style lang="scss" scoped>
.contact-form {
  @include screen(large) {
    @include content-grid;

    form,
    aside {
      grid-row: 1 / -1;
    }

    form {
      grid-column: 7 / -1;
      width: 100%;
    }

    aside {
      grid-column: 1 / 7;
    }
  }

  @include screen(x-large) {
    @include content-grid;
    aside {
      grid-column: 2 / 7;
    }
  }
}
aside {
  // padding: $spacing-lg 0;

  h3 {
    font-size: scale('h2');
    font-weight: 900;

    color: $neutral-500;

    width: fit-content;
    margin-bottom: $spacing-md;
  }

  @include screen(large) {
    padding: $spacing-lg;
  }
}
.aside__social {
  padding: $spacing-md 0;
}

form {
  @include screen(medium) {
    // max-width: rem(450);
    padding: $spacing-lg;
    margin: auto;
  }

  @include screen(large) {
    padding: $spacing-lg;
  }
  @include screen(x-large) {
    padding: $spacing-lg $spacing-lg * 3;
  }
}

.form-group {
  @include flex-wrap-col;
  padding: $spacing-sm 0;

  label {
    font-size: scale('h5');
    font-weight: 400;
    padding: $spacing-sm 0;
    color: $neutral-900;
  }
  .form-control {
    padding: $spacing-sm $spacing-md;
    background-color: $neutral-50;
    border: rem(1) solid $neutral-500;
  }

  .submit-btn {
    width: 100%;
  }
}
</style>
