<template>
  <div>
    <h1>Footer TBD</h1>
    <form name="buySki" method="POST" data-netlify="true">
      <p>
        <label>
          Your Name:
          <input type="text" name="name">
        </label>
      </p>
      <p>
        <label>
          Your Email:
          <input type="email" name="email">
        </label>
      </p>
      <p>
        <label>
          Your Role:
          <select name="role[]" multiple>
            <option value="leader">Leader</option>
            <option value="follower">Follower</option>
          </select>
        </label>
      </p>
      <p>
        <label>
          Message:
          <textarea name="message"></textarea>
        </label>
      </p>
      <p>
        <button type="submit">Send</button>
      </p>
    </form>
  </div>
</template>

<script>
export default {
  name: "Footer"
};
</script>

<style scoped>
h1 {
  text-align: center;
}
</style>
