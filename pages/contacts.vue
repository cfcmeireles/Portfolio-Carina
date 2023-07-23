<template>
  <main id="contacts-page">
    <div class="contacts">
      <h1 class="section-titles">Contact me</h1>
      <form>
        <label for="name">Name</label>
        <input type="text" id="name" placeholder="Your name" />
        <label for="email">Email</label>
        <input type="text" id="email" placeholder="Your email" />
        <label for="subject">Subject</label>
        <textarea id="subject" placeholder="Write here"></textarea>
        <input type="submit" value="Submit" />
      </form>
    </div>
  </main>
</template>
    
<script >
</script>
    
    <style>
input[type="text"],
textarea {
  width: 100%;
  padding: 12px;
  border: 1px solid #ccc;
  border-radius: 4px;
  box-sizing: border-box;
  margin-top: 6px;
  margin-bottom: 16px;
  resize: vertical;
}

input[type="submit"] {
  background-color: #04aa6d;
  color: white;
  padding: 12px 20px;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

input[type="submit"]:hover {
  background-color: #45a049;
}

/* .contacts {
  border-radius: 5px;
  background-color: #f2f2f2;
  padding: 50px;
} */
</style>