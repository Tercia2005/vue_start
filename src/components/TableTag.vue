<template>

    <tr  v-if="typeof t.dates == 'string'">
                <td data-label="Employee">{{ t?.employeeName }}</td>
                <td data-label="Number">{{ t?.employeeNum }}</td>
                <td  data-label="Dates">{{ t?.dates }}</td>
                <td data-label="Reason">{{ t?.reason }}</td>
                        <td data-label="Status">{{ t?.status }}</td>
                        <td data-label="Action">
                            <button class="button1" @click="updateRequestStatus(t.id, 'Approved')">Approve</button>
                            <button class="button2"  @click="openDenyModal(index)">Deny</button>
                           
                        </td>
                    
    </tr>

    <tr v-else v-for="d,index in t.dates">
                <td data-label="Employee">{{ t?.employeeName }}</td>
                <td data-label="Number">{{ t?.employeeNum }}</td>
                <td  data-label="Dates">{{ d?.dates }}</td>
                <td data-label="Reason">{{ d?.reason }}</td>
                        <td data-label="Status">{{ d?.status }}</td>
                        <td data-label="Action">
                            <button class="button1" @click="updateRequestStatus(index, 'Approved')">Approve</button>
                            <button class="button2" @click="openDenyModal(index)">Deny</button>
                        </td>

                        
                        
        </tr>
        <div v-if="showModal" class="modal">
        <h3>Enter reason for denial</h3>
    <input v-model="hrcom" type="text" >
    <button @click="submitDenyComment">Confirm Denial</button>
    <button @click="showModal=true">Cancel</button>

</div>

    </template>
    
    

<script>
import { Modal } from 'bootstrap';


export default {
    data(){
        return{
        }
    },
    props:['t'],
    name: 'MyModal',
    methods:{
        updateRequestStatus(index, newStatus) {
            if (this.t.status) {
                this.t.status = newStatus;
            } else{
                this.t.dates[index].status = newStatus
            }
            
        },
        showModal(){
            const modalElement = this.$refs.modal;
            const modalInstance = new Modal(modalElement);
            modalInstance.show();
        }
    }
}
</script>
<style>
button{
    margin-right: 10px;
}
    .button1{
    background-color: lightgreen;
    border-radius: 6px;

}
 
  .button2{
    background-color: lightcoral;
    border-radius: 5px;
  }
</style>