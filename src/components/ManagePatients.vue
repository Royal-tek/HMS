<template>
    <div class="holder">
        <div class="container-fluid">
        <h1 class="text-center manage-patient-text my-3">Manage Patients</h1>
        <table class="table table-bordered table-striped table-hover table-responsive">
            
            <tr>
                <th>NS</th>
                <th>Patient full Name</th>
                <th>Patient Condition</th>
                <th>Prescriptions carried out</th>
                <th>Prescriptions to be ccarried out</th>
                <th>Date in</th>
                <th>Estimated Date Out</th>
             
            </tr>
            <tr>
                <td><b>1</b></td>
                <td class="text-capitalize">Chijike amadi</td>
                <td>Malaria and breathing difficulty</td>
                <td>2 injections with melanin</td>
                <td>heart transplant</td>
                <td>20-09-12</td>
                <td>29-45-66</td>
                
            </tr>

    
      
        </table>
        </div>
    </div>
</template>

<script>
export default {
    name : 'ManagePatients',
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
.manage-patient-text::after{
  display: block;
  content: '';
  width: 50px;
  height: 3px;
  margin: 10px auto;
  background-color: #1067cad3;
}
</style>