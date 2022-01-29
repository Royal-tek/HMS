<template>
    <div class="holder">
        <div class="container-fluid">
        <h1 class="text-center manage-hospital-text my-3">Manage Hospitals</h1>
        <table class="table table-bordered table-striped table-hover table-responsive">
            
            <tr>
                <th>NS</th>
                <th>Hospital Name</th>
                <th>Ownership</th>
                <th>Location</th>
                <th>Contact Number</th>
                <th>Action</th>
             
            </tr>
            <tr>
                <td><b>1</b></td>
                <td>Protek</td>
                <td>Private</td>
                <td>1 ammi close rumuodara</td>
                <td>09025747042</td>
                <td>
                    <input type="button" value="X" class="form-control bg-danger text-white shadow-none">
                </td>
            </tr>

             <tr>
                <td><b>2</b></td>
                <td>Protek</td>
                <td>Private</td>
                <td>1 ammi close rumuodara</td>
                <td>09025747042</td>
                <td>
                    <input type="button" value="X" class="form-control bg-danger text-white shadow-none">
                </td>
            </tr>
      
        </table>
        </div>
    </div>
</template>

<script>
export default {
    name : 'ManageHospitals',
}
</script>

<style scoped lang="scss">
.holder{
    display: flex;
    align-items: center;
    justify-content: center;
}
@media (max-width:600px){
    table{
        font-size: 12px;
    }

    table td {
        padding: 5px;
    }
}
.manage-hospital-text::after{
  display: block;
  content: '';
  width: 50px;
  height: 3px;
  margin: 10px auto;
  background-color: #1067cad3;
}
</style>