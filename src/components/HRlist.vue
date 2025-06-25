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
                dates:"22-07-2025",
                reason:"Sick Leave",
                status:"Pending",
                comment: ""
            },
            {
                dates:"01-12-2024",
                reason:"Personal",
                status:"Pending",
                comment: ""
            }]
    
        },  
        {  id : 2  ,
            employeeName : "Lungile Moyo" ,
            employeeNum : 654321,
            dates: [{
                status : "Pending",
                dates : "15-07-2025",
                reason : "Family Responsibilty",
                comment: ""
                
            
            },{
                dates : "02-12-2024",
                reason : "Vacation", 
                status : "Pending",
                comment: ""
            }
        ]

            
    
        },
        {  id : 3  ,
            employeeName : "Thabo Molefe",
            employeeNum : 147896,
            dates: [{
                status : "Pending",
                dates : "10-07-2025",
                reason : "Medical Appointment",
                comment: ""

            },{
                dates : "05-12-2024",
                reason : "Personal",
                status : "Pending",
                comment: ""

            }
    
        ]
            
    
        },
        {   id : 4 ,
            employeeName : "Keshav Naidoo",
            employeeNum : 369871,
            status : "Pending", 
            dates : "20-07-2025",
            reason : "Bereavement",
            comment: ""
            
            
    
        },
        {   id : 5 ,
            employeeName : "Zanele Khumalo",
            employeeNum : 789456,
            status : "Pending",
            dates : "01-12-2024",
            reason: "ChildCare",
            comment: ""
            
    
        },
        {   id : 6 ,
            employeeName : "Sipho Zulu",
            employeeNum : 654987,
            status : "Pending",
            dates : "18-07-2025",
            reason: "Sick Leave",
            comment: ""
            
    
        },
        {   id : 7 , 
            employeeName : "Naledi Moeketsi",
            employeeNum : 258963,
            status : "Pending",
            dates : "22-07-2025",
            reason : "Vacation",
            comment: ""

            
    
        },
        {   id : 8  ,
            employeeName : "Farai Gumbo",
            employeeNum : 147852,
            status : "Pending",
            dates: "02-12-2024",
            reason: "Medical Appointment",
            comment: ""

            
    
        },
        {   id : 9 ,
            employeeName : "Karabo Dlamini",
            employeeNum : 159632,
            status : "Pending",
            dates: "19-07-2025",
            reason: "Childcare",
            comment: ""

            
    
        },
        {   id : 10 , 
            employeeName : "Fatima Patel",
            employeeNum : 357412,
            status : "Pending",
            dates: "03-12-2024",
            reason: "Vacation",
            comment: ""

            
    
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