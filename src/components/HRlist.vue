<template>
    <table border="2">
        <thead>
            <tr>
                <th>EmployeeName</th>
                <th>EmployeeNo.</th>
                <th>Dates</th>
                <th>Reason</th>
                <th>Status</th>
                <th>Action</th>
               
            </tr>
        </thead>
        <tbody>
            <table-tag v-for="t in requests" :t="t"/>
            
             
        </tbody>
    </table>
</template>

<script>
import TableTag from './TableTag.vue'


export default{
    components:{
        TableTag
    },

    data(){

        return{
            requests: [

        {  id : 1 ,  
            employeeName : "Sibongile Nkosi",
            employeeNum : 123456 ,
            dates : [{
                dates:"2025-07-22",
                reason:"Sick Leave",
                status:"Pending"
            },
            {
                dates:"2024-12-01",
                reason:"Personal",
                status:"Pending"
            }]
    
        },  
        {  id : 2  ,
            employeeName : "Lungile Moyo" ,
            employeeNum : 654321,
            dates: [{
                status : "Pending",
                dates : "2025-07-15",
                reason : "Family Responsibilty",
            },{
                dates : "2024-12-02",
                reason : "Vacation", 
                status : "Pending"
            }
        ]

            
    
        },
        {  id : 3  ,
            employeeName : "Thabo Molefe",
            employeeNum : 147896,
            dates: [{
                status : "Pending",
                dates : "2025-07-10",
                reason : "Medical Appointment",

            },{
                dates : "2024-12-05",
                reason : "Personal",
                status : "Pending"

            }
    
        ]
            
    
        },
        {   id : 4 ,
            employeeName : "Keshav Naidoo",
            employeeNum : 369871,
            status : "Pending", 
            dates : "2025-07-20",
            reason : "Bereavement",
            
            
    
        },
        {   id : 5 ,
            employeeName : "Zanele Khumalo",
            employeeNum : 789456,
            status : "Pending",
            dates : "2024-12-01",
            reason: "ChildCare"
            
    
        },
        {   id : 6 ,
            employeeName : "Sipho Zulu",
            employeeNum : 654987,
            status : "Pending",
            dates : "2025-07-18",
            reason: "Sick Leave",
            
    
        },
        {   id : 7 , 
            employeeName : "Naledi Moeketsi",
            employeeNum : 258963,
            status : "Pending",
            dates : "2025-07-22",
            reason : "Vacation"

            
    
        },
        {   id : 8  ,
            employeeName : "Farai Gumbo",
            employeeNum : 147852,
            status : "Pending",
            dates: "2024-12-02",
            reason: "Medical Appointment",

            
    
        },
        {   id : 9 ,
            employeeName : "Karabo Dlamini",
            employeeNum : 159632,
            status : "Pending",
            dates: "2025-07-19",
            reason: "Childcare",

            
    
        },
        {   id : 10 , 
            employeeName : "Fatima Patel",
            employeeNum : 357412,
            status : "Pending",
            dates: "2024-12-03",
            reason: "Vacation",

            
    
        },
        


            ]
        };
    },

    methods: {
       
       
    }
}

</script>

<style>
thead{
 background-color: lightblue;

}
tbody{
    background-color: beige;
    

}

.section{
  height: 700px;
  background-color: ;
  z-index: 999;

}
table{
  border: 2px solid black;
  border-radius: 10px; 
  min-width: 40%;
  margin-left: 15%;
  z-index: -1;
  width: 70%;
  border-color: black;

}
thead, th, td {
  padding: 1rem;
  text-align: center;
  font-size: 1rem;
}



</style>