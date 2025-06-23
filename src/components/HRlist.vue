<template>
    <table>
        <thead>
            <tr>
                <th>Employee</th>
                <th>Status</th>
                <th>Action</th>
            </tr>
        </thead>
        <tbody>
            <RequestRow 
             v-for = "t in requests"
             :key="t.id"
             :request="t"

             @approve="updateRequestStatus(t.id , 'Approved')"

             @deny="updateRequestStatus(t.id , 'Denied')"
             />
             
        </tbody>
    </table>
</template>

<script>
import RequestRow from '@/components/RequestRow.vue';

export default{

    components:{
        RequestRow
    },

    data(){
        return{
            requests: [

        { id : 1 ,  
            employeeName : "Tercia Abrahams",
            employeeNum : 123456 ,
            status : "Pending"
            
    
        },
        {id : 2  ,
            employeeName : "Cameron Jacobs" ,
            employeeNum : 654321,
            status : "Pending"
            
    
        },
        {id : 3  ,
            employeeName : "Keegan Philander",
            employeeNum : 147896,
            status : "Pending"
            
    
        },
        {id : 4 ,
            employeeName : "Thabo Mdaki",
            employeeNum : 36987,
            status : "Pending"
            
    
        },
        {id : 5 ,
            employeeName : "Lisa Bonnet",
            employeeNum : 789456,
            status : "Pending"
            
    
        },
        {id : 6 ,
            employeeName : "Jessica Andres",
            employeeNum : 654987,
            status : "Pending"
            
    
        },
        {id : 7 , 
            employeeName : "Lia Giselle",
            employeeNum : 258963,
            status : "Pending"
            
    
        },
        {id : 8  ,
            employeeName : "Brandon Lopez",
            employeeNum : 147852,
            status : "Pending"
            
    
        },
        {id : 9 ,
            employeeName : "Penelope Cruz",
            employeeNum : 159632,
            status : "Pending"
            
    
        },
        {id : 10 , 
            employeeName : "Siya Bdeni",
            employeeNum : 357412,
            status : "Pending"
            
    
        },



            ]
        };
    },

    methods: {
        updateRequestStatus(id, newStatus) {
            const request = this.requests.find(t => t.id === id);
            if (request) {
                request.status = newStatus;
            }
        }
    }
}

</script>