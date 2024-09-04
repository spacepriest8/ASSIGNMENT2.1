#

const student0 ={
    name:"peter",
    age:20,
    grade:60,
};
const student1 ={
    name:"samuel",
    age:23,
    grade:77,
};
const student2={
    name:"chikoadi",
    age:25,
    grade:96,
};
const student3={
    name:"okeke",
    age:40,
    grade:88,
};
const student4={
    name:"oluwatosin",
    age:27,
    grade:69,
};
const student5={
    name:"chris",
    age:20,
    grade:50,
};
const student6={
    name:"king",
    age:30,
    grade:100,
};
filterBygrade =[student0,student1,student2,student3,student4,student5,student6];
filterBygrade.forEach((student,index) => {
    if(student.grade>= 70){
        console.log(`${index}`);
    console.log(`name: ${student.name}, Grade: ${student.grade}`);
    }
});

//Function that calculates the average age
const calculateaverageAge=(filterBygrade)=> {
    if (filterBygrade.length === 0)
        return`no student available`;
    const totalAge = filterBygrade.reduce((sum,student) => sum + student.age, 0);
    return totalAge/filterBygrade.length;
};
const averageAge = calculateaverageAge(filterBygrade);
console.log(`The average age of student is ${averageAge.toFixed(4)}`); //to 4 decimal place
 
