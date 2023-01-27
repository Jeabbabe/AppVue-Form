<script setup>
import HelloWorld from "./components/HelloWorld.vue";
import TheWelcome from "./components/TheWelcome.vue";
</script>

<template>
  <page size="A4">
    <h5>
      <form class="head">
        แบบแสดงรายงานการกระจายการถือหุ้น<br />
        บริษัท <input type="text" /> จํากัด (มหาชน)<br /><br />
        ณ วันที่ <input type="date" />
      </form>
    </h5>
    <form style="text-indent: 50px">
      ทุนจดทะเบียนที่เรียกชำระแล้ว (เฉพาะหุ้นสามัญ)
      <input type="text" size="10" /> บาท แบ่งเป็นหุ้นสามัญ
      <input type="text" size="10" /> หุ้น มูลค่าที่ตราไว้หุ้นละ
      <input type="text" size="10" /> บาท
    </form>
    <table>
      <tr>
        <th width="54%">ผู้ถือหุ้นสามัญ</th>
        <th>จำนวนราย</th>
        <th>จำนวนหุ้น</th>
        <th width="18%">% ของทุนชำระแล้ว<br />(เฉพาะหุ้นสามัญ)</th>
      </tr>
      <tr>
        <td class="bold" colspan="4">1. ผู้ถือหุ้นสามัญที่เป็น</td>
      </tr>
      <tr>
        <td class="margin">
          1.1 กรรมการ ผู้จัดการ และผู้บริหาร รวมถึงผู้เกี่ยวข้อง และบุคคลที่มีความสัมพันธ์
        </td>
        <td class="body"><input type="text" size="7.5" /></td>
        <td class="body"><input type="text" size="7.5" /></td>
        <td class="body"><input type="text" size="10" /></td>
      </tr>
      <tr>
        <td class="margin">
          1.2 ผู้ถือหุ้นสามัญที่ถือหุ้นมากกว่า 5% โดยนับรวมผู้เกี่ยวข้องด้วย
        </td>
        <td class="body"><input type="text" size="7.5" /></td>
        <td class="body"><input type="text" size="7.5" /></td>
        <td class="body"><input type="text" size="10" /></td>
      </tr>
      <tr>
        <td class="margin">1.3 ผู้มีอำนาจควบคุม</td>
        <td class="body"><input type="text" size="7.5" /></td>
        <td class="body"><input type="text" size="7.5" /></td>
        <td class="body"><input type="text" size="10" /></td>
      </tr>
      <tr>
        <td class="bold">2. ผู้ถือหุ้นสามัญรายย่อยที่ถือไม่ต่ำกว่า 1 หน่วยการซื้อขาย</td>
        <td class="body"><input type="text" size="7.5" /></td>
        <td class="body"><input type="text" size="7.5" /></td>
        <td class="body"><input type="text" size="10" /></td>
      </tr>
      <tr>
        <td class="bold">3. ผู้ถือหุ้นสามัญที่ถือต่ำกว่า 1 หน่วยการซื้อขาย</td>
        <td class="body"><input type="text" size="7.5" /></td>
        <td class="body"><input type="text" size="7.5" /></td>
        <td class="body"><input type="text" size="10" /></td>
      </tr>
      <tr>
        <td class="bold center">รวมจำนวนผู้ถือหุ้นสามัญทั้งสิ้น</td>
        <td class="bold body"><input type="text" size="8" /></td>
        <td class="bold body"><input type="text" size="8" /></td>
        <td class="bold body"><input type="text" size="12" /></td>
      </tr>
    </table>
    <form style="text-align: right">
      บริษัทขอรับรองว่าสารสนเทศที่ได้รายงานไว้ในหนังสือรับรองฉบับนี้ถูกต้อง<br />
      ลงชื่อ <input type="text" size="30" /> <br />ตำแหน่ง <input type="text" size="35" />
    </form>
  </page>
</template>

<style scoped>
body {
  background: rgb(204, 204, 204);
}
page {
  background: white;
  display: block;
  margin: 1cm auto;
  box-shadow: 0 0 0.5cm rgba(0, 0, 0, 0.5);
}
page[size="A4"] {
  width: 21cm;
  height: 29.7cm;
  padding: 0.5cm;
}
.head {
  margin-bottom: 0.5cm;
  text-align: center;
  font-weight: bold;
  color: black;
}
.bold {
  font-weight: bold;
}
input[type="text"] {
  border: none;
  border-bottom: 2px dotted black;
}
table,
th,
td {
  border: 1px solid black;
}
table {
  margin-block: 20px;
}
th {
  text-align: center;
  font-weight: bold;
}
.margin {
  padding-left: 20px;
}
td.body {
  text-align: center;
  padding-bottom: 10px;
}
.center {
  text-align: center;
}
</style>
