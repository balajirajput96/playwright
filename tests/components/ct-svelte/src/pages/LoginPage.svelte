<script>
let username = '';
let password = '';

function handleSubmit(event) {
  event.preventDefault();
  console.log('Login attempted', { username, password });
}
</script>

<main>
  <h2>Login</h2>
  <form on:submit={handleSubmit}>
    <div>
      <label for="username">Username or email address</label>
      <input
        id="username"
        bind:value={username}
        type="text"
        placeholder="Enter username"
      />
    </div>
    <div>
      <label for="password">Password</label>
      <input
        id="password"
        bind:value={password}
        type="password"
        placeholder="Enter password"
      />
    </div>
    <button type="submit">Sign in</button>
  </form>
</main>
