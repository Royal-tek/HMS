<template>
  <div class="holder">
    <form action="" class="addhospital-form bg-white">
      <h1 class="add-hospital-text text-center my-2">Add Hospital</h1>
      <div class="row">
        <div class="col-md-6">
          <div class="input-group">
            <input
              type="text"
              class="form-control shadow-none"
              placeholder="Hospital Name"
            />
          </div>
        </div>
        <div class="col-md-6">
          <div class="input-group">
            <input
              type="text"
              class="form-control shadow-none"
              placeholder="Hospital Location"
            />
          </div>
        </div>
      </div>
      <div class="row">
          <div class="col-md-6">
          <div class="input-group">
              <select name="" id="" class="form-control">
                  <option value="">*** Select Ownership ***</option>
                  <option value="private">Private</option>
                  <option value="government">Government</option>
              </select>
          </div>
        </div>

        <div class="col-md-6">
          <div class="input-group">
            <input
              type="number"
              class="form-control shadow-none"
              placeholder="Contact Number"
            />
          </div>
        </div>
        
      </div>
      <input type="submit" class="btn hospital-button" value="Submit">
      
    </form>
  </div>
</template>

<script>
export default {
  name: "AddHospital",
};
</script>

<style scoped lang="scss">

form {
  width: 100%;
  margin: 0 auto;
}
.input-group {
  width: 100%;

  input {
    padding: 15px 20px;
    margin: 10px 0;
  }
}
.add-hospital-text::after{
  display: block;
  content: '';
  width: 50px;
  height: 3px;
  margin: 10px auto;
  background-color: #1067cad3;
}
.hospital-button{
    width: 100%;
    background-color: #1067cad3;
    font-size: 17px;
    font-weight: bold;
    transition: .5s;
    padding: 15px 20px;
    color: #fff;

    &:hover{
        background-color: #074388d3;
    }
}
</style>