<template>
  <h3>학생정보</h3>
    <table>
        <tr>
            <td>이름 :</td>
            <td>{{name}}</td> 
        </tr>
        <tr>
            <td>학년 :</td>
            <td>{{grade}}</td>
        </tr>
        <tr>
            <td>분류</td>
            <td><slot name="studentInfo"></slot></td>
        </tr>
    </table>
</template>

<script>
    export default {
        props : ['name', 'grade'],
        data() {

        }  
    };
</script>