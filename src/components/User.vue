<template>
    <span className="user">
      <span className="name">{{ name }}</span>
      <span className="handle">{{ handle }}</span>
    </span>
  </template>
  
  <script>
  export default {
    props: {
      name: {
        type: String,
      },
      handle: {
        type: String,
      },
    },
  };
  </script>
  
  <style></style>