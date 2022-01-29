<template>
    <div class="holder">
        <div class="container-fluid">
            <h1 class="text-center refer-text my-3">Referrals</h1>
            
        <table class="table table-bordered table-striped table-hover ">
            
            <tr>
                <th>NS</th>
                <th>Patient Full Name</th>
                <th>Patient Email Address</th>
                <th>Patient Contact Number</th>
                <th>Patient Hospital</th>
                <th>Patient Age</th>
                <th>Patient Gender</th>
                <th>Patient DOB</th>
                <th>Patient Image</th>
                <th>Patient Condition</th>

             
             
            </tr>
            <tr>
                <td><b>1</b></td>
                <td>Afonime Royal</td>
                <td>afonimeroyal@gmail.com</td>
                <td>Protek</td>
                <td>09025747042</td>
                <td>20</td>
                <td>Male</td>
                <td>30-05-2001</td>
                <td>
                    <div class="patient-image-holder">
                    <img src="images/patient.jpg" class="img-fluid patient-image">
                    </div>
                </td>
                <td>Lorem ipsum dolor sit amet consectetur adipisicing elit. Excepturi laudantium distinctio ducimus voluptatum praesentium, doloremque totam voluptas quam rem atque!</td>
                
            </tr>

      
        </table>
        </div>
    </div>
</template>

<script>
export default {
    name : 'ManageRefers',
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
.patient-image-holder{
    width: 100px;
    height: 100px;
    overflow: hidden;
}
table{
    font-size: 14px;
    height: 10px;
}
.refer-text::after{
    content: '';
    display: block;
    margin: 10px auto;
    background-color: #1067cad3;
    width: 50px;
    height: 3px;
}
</style>