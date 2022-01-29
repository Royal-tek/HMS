    <template>
  <Navbar />
  <div class="holder">
    <div class="container">
      <div class="card form-card">
        <form action="" class="refer-form">
        <h1 class="refer-first-text text-center text-capitalize my-3">Patient Registration</h1>
          <div class="row">
            <div class="col-md-6">
              <div class="input-group">
                <input type="text" class="form-control shadow-none" placeholder="Patient First Name"  />
              </div>
            </div>
            <div class="col-md-6">
              <div class="input-group">
                <input type="text" class="form-control shadow-none" placeholder="Patient Last Name"  />
              </div>
            </div>
          </div>

          <div class="row">
            <div class="col-md-6">
              <div class="input-group">
                <input type="text" class="form-control shadow-none" placeholder="Patient Email Address"  />
              </div>
            </div>
            <div class="col-md-6">
              <div class="input-group">
                <input type="number" class="form-control shadow-none" placeholder="Patient Phone Number"  />
              </div>
            </div>
          </div>

          <div class="row">
              <div class="col-md-6">
              <div class="input-group">
                <input type="text" class="form-control shadow-none" placeholder="Patient Hospital"  />
              </div>
            </div>

            <div class="col-md-6">
                <label for="">Patient Image:</label>
                <div class="input-group">
                    <input type="file" class="form-control shadow-none" />
                </div>
            </div>
            <!-- <div class="col-md-7"> -->
              <!-- <div class="input-group"> -->
                  <!-- <textarea  class="form-control shadow-none" placeholder="Description Of Condition"></textarea> -->
                <!-- <input type="text" class="form-control shadow-none" placeholder="Patient First Name"  /> -->
              <!-- </div> -->
            <!-- </div> -->
            
          </div>

          <div class="row my-2">
            <div class="col-md-4">
              <div class="input-group">
                <input type="number" class="form-control shadow-none" placeholder="Patient Age"  />
              </div>
            </div>
            <div class="col-md-4">
              <div class="input-group">
                  <select name="" id="" class="form-control shadow-none">
                      <option value="">Gender</option>
                      <option value="">Male</option>
                      <option value="">Female</option>
                  </select>
                
              </div>
            </div>
            <div class="col-md-4">
                 <label for="">Patient DOB:</label>
              <div class="input-group">
                <input type="date" class="form-control shadow-none" />
              </div>
            </div>
            

          </div>
          <div class="input-group">
              <input type="submit" class="btn refer-button">
          </div>

        </form>
      </div>
    </div>
  </div>
</template>

<script>
import Navbar from "../components/Navbar.vue";
export default {
  name: "PatientRegister",
  components: {
    Navbar,
  },
};
</script>

    <style scoped lang="scss">
.holder {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 100%;
    background: radial-gradient(rgba(42, 42, 46, 0.7), rgba(148, 151, 199, 0.5)) , url(/images/patient.jpg);
    height: calc(100vh - 94px);
    background-position: center;
    background-attachment: fixed;
    background-size: cover;
}
.refer-first-text::after{
    display: block;
    width: 50px;
    height: 3px;
    content: '';
    background-color: #1067cad3;
    margin: 10px auto;
}
.form-card {
    padding: 20px 30px;
    max-width: 85%;
    margin: 0 auto;
    border-radius: 10px;

}
.input-group{
    margin: 10px 0;
    
    input{
        padding: 15px 15px;
        
    }
}
.refer-button{
    background-color: #1067cad3;
    color: white;
    margin: 0 auto;
    width: 100%;
    font-size: 20px;
    font-weight: bold;
}
.refer-button:hover{
    background-color: #073f80d3;
}
</style>