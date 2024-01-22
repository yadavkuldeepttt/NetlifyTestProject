<script>
  import axios from "axios";
  let username = "";
  let userpassword = "";

  const saveLoginDetails = async () => {
    try {
      const response = await axios.post(
        "http://localhost:4747/api/users/add-user",
        {
          username,
          userpassword,
        }
      );
      console.log("User added:", response.data);
      alert("User added");
      username = "";
      userpassword = "";
    } catch (err) {
      console.error("Error adding calendar:", err.message);
    }
  };
</script>

<div>Hello World</div>

<div>
  <form action="">
    <input
      type="text"
      class="form-control"
      bind:value={username}
      placeholder="Enter username"
    />
    <input
      type="text"
      class="form-control"
      bind:value={userpassword}
      placeholder="Enter user password"
    />
    <button class="btn btn-primary" on:click={saveLoginDetails}>Save</button>
  </form>
</div>
