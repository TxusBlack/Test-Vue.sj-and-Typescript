<template>
  <div class="hello">

    <div class="row">
      <div class="col">
        <select class="browser-default custom-select" v-model="fecha.dia">
          <option value="" selected>Seleccionar día</option>
          <option value="lun">Lunes</option>
          <option value="mar">Martes</option>
          <option value="mie">Miércoles</option>
          <option value="jue">Jueves</option>
          <option value="vie">Viernes</option>
          <option value="sab">Sábado</option>
          <option value="dom">Domingo</option>
        </select>
      </div>
      <div class="col">
        <select class="browser-default custom-select" v-model="fecha.horarioInicial">
          <option value="" selected>Horario Incial</option>
          <option value="6">6:00</option>
          <option value="6-3">6:30</option>
          <option value="7">7:00</option>
          <option value="7-3">7:30</option>
          <option value="8">8:00</option>
          <option value="8-3">8:30</option>
          <option value="9">9:00</option>
          <option value="9-3">9:30</option>
          <option value="10">10:00</option>
          <option value="10-3">10:30</option>
          <option value="11">11:00</option>
          <option value="11-3">11:30</option>
          <option value="12">12:00</option>
          <option value="12-3">12:30</option>
          <option value="13">13:00</option>
          <option value="13-3">13:30</option>
          <option value="14">14:00</option>
          <option value="14-3">14:30</option>
          <option value="15">15:00</option>
          <option value="15-3">15:30</option>
          <option value="16">16:00</option>
          <option value="16-3">16:30</option>
          <option value="17">17:00</option>
          <option value="17-3">17:30</option>
          <option value="18">18:00</option>
          <option value="18-3">18:30</option>
          <option value="19">19:00</option>
          <option value="19-3">19:30</option>
          <option value="20">20:00</option>
        </select>
      </div>
      <div class="col">
        <select class="browser-default custom-select" v-model="fecha.horarioFinal">
          <option value="" selected>Horario Final</option>
          <option value="6">6:00</option>
          <option value="6-3">6:30</option>
          <option value="7">7:00</option>
          <option value="7-3">7:30</option>
          <option value="8">8:00</option>
          <option value="8-3">8:30</option>
          <option value="9">9:00</option>
          <option value="9-3">9:30</option>
          <option value="10">10:00</option>
          <option value="10-3">10:30</option>
          <option value="11">11:00</option>
          <option value="11-3">11:30</option>
          <option value="12">12:00</option>
          <option value="12-3">12:30</option>
          <option value="13">13:00</option>
          <option value="13-3">13:30</option>
          <option value="14">14:00</option>
          <option value="14-3">14:30</option>
          <option value="15">15:00</option>
          <option value="15-3">15:30</option>
          <option value="16">16:00</option>
          <option value="16-3">16:30</option>
          <option value="17">17:00</option>
          <option value="17-3">17:30</option>
          <option value="18">18:00</option>
          <option value="18-3">18:30</option>
          <option value="19">19:00</option>
          <option value="19-3">19:30</option>
          <option value="20">20:00</option>
        </select>
      </div>
    </div>

    <mdb-btn color="primary" @click="crearHorario">Agendar</mdb-btn>

    <mdb-tbl responsive>
      <mdb-tbl-head>
        <tr>
          <th>Hora</th>
          <th>Lunes</th>
          <th>Martes</th>
          <th>Miércoles</th>
          <th>Jueves</th>
          <th>Viernes</th>
          <th>Sábado</th>
          <th>Domingo</th>
        </tr>
      </mdb-tbl-head>
      <mdb-tbl-body>
        <tr>
          <th>6:00</th>
          <td v-bind:class="{ active: estilosHorarios.lun6 }" class="lun-6"></td>
          <td v-bind:class="{ active: estilosHorarios.mar6 }" class="mar-6"></td>
          <td v-bind:class="{ active: estilosHorarios.mie6 }" class="mie-6"></td>
          <td v-bind:class="{ active: estilosHorarios.jue6 }" class="jue-6"></td>
          <td v-bind:class="{ active: estilosHorarios.vie6 }" class="vie-6"></td>
          <td v-bind:class="{ active: estilosHorarios.sab6 }" class="sab-6"></td>
          <td v-bind:class="{ active: estilosHorarios.dom6 }" class="dom-6"></td>
        </tr>
        <tr>
          <th>6:30</th>
          <td v-bind:class="{ active: estilosHorarios.lun63 }" class="lun-6-3"></td>
          <td v-bind:class="{ active: estilosHorarios.mar63 }" class="mar-6-3"></td>
          <td v-bind:class="{ active: estilosHorarios.mie63 }" class="mie-6-3"></td>
          <td v-bind:class="{ active: estilosHorarios.jue63 }" class="jue-6-3"></td>
          <td v-bind:class="{ active: estilosHorarios.vie63 }" class="vie-6-3"></td>
          <td v-bind:class="{ active: estilosHorarios.sab63 }" class="sab-6-3"></td>
          <td v-bind:class="{ active: estilosHorarios.dom63 }" class="dom-6-3"></td>
        </tr>
        <tr>
          <th>7:00</th>
          <td v-bind:class="{ active: estilosHorarios.lun7 }" class="lun-7"></td>
          <td v-bind:class="{ active: estilosHorarios.mar7 }" class="mar-7"></td>
          <td v-bind:class="{ active: estilosHorarios.mie7 }" class="mie-7"></td>
          <td v-bind:class="{ active: estilosHorarios.jue7 }" class="jue-7"></td>
          <td v-bind:class="{ active: estilosHorarios.vie7 }" class="vie-7"></td>
          <td v-bind:class="{ active: estilosHorarios.sab7 }" class="sab-7"></td>
          <td v-bind:class="{ active: estilosHorarios.dom7 }" class="dom-7"></td>
        </tr>
        <tr>
          <th>7:30</th>
          <td v-bind:class="{ active: estilosHorarios.lun73 }" class="lun-7-3"></td>
          <td v-bind:class="{ active: estilosHorarios.mar73 }" class="mar-7-3"></td>
          <td v-bind:class="{ active: estilosHorarios.mie73 }" class="mie-7-3"></td>
          <td v-bind:class="{ active: estilosHorarios.jue73 }" class="jue-7-3"></td>
          <td v-bind:class="{ active: estilosHorarios.vie73 }" class="vie-7-3"></td>
          <td v-bind:class="{ active: estilosHorarios.sab73 }" class="sab-7-3"></td>
          <td v-bind:class="{ active: estilosHorarios.dom73 }" class="dom-7-3"></td>
        </tr>
        <tr>
          <th>8:00</th>
          <td v-bind:class="{ active: estilosHorarios.lun8 }" class="lun-8"></td>
          <td v-bind:class="{ active: estilosHorarios.mar8 }" class="mar-8"></td>
          <td v-bind:class="{ active: estilosHorarios.mie8 }" class="mie-8"></td>
          <td v-bind:class="{ active: estilosHorarios.jue8 }" class="jue-8"></td>
          <td v-bind:class="{ active: estilosHorarios.vie8 }" class="vie-8"></td>
          <td v-bind:class="{ active: estilosHorarios.sab8 }" class="sab-8"></td>
          <td v-bind:class="{ active: estilosHorarios.dom8 }" class="dom-8"></td>
        </tr>
        <tr>
          <th>8:30</th>
          <td v-bind:class="{ active: estilosHorarios.lun83 }" class="lun-8-3"></td>
          <td v-bind:class="{ active: estilosHorarios.mar83 }" class="mar-8-3"></td>
          <td v-bind:class="{ active: estilosHorarios.mie83 }" class="mie-8-3"></td>
          <td v-bind:class="{ active: estilosHorarios.jue83 }" class="jue-8-3"></td>
          <td v-bind:class="{ active: estilosHorarios.vie83 }" class="vie-8-3"></td>
          <td v-bind:class="{ active: estilosHorarios.sab83 }" class="sab-8-3"></td>
          <td v-bind:class="{ active: estilosHorarios.dom83 }" class="dom-8-3"></td>
        </tr>
        <tr>
          <th>9:00</th>
          <td v-bind:class="{ active: estilosHorarios.lun9 }" class="lun-9"></td>
          <td v-bind:class="{ active: estilosHorarios.mar9 }" class="mar-9"></td>
          <td v-bind:class="{ active: estilosHorarios.mie9 }" class="mie-9"></td>
          <td v-bind:class="{ active: estilosHorarios.jue9 }" class="jue-9"></td>
          <td v-bind:class="{ active: estilosHorarios.vie9 }" class="vie-9"></td>
          <td v-bind:class="{ active: estilosHorarios.sab9 }" class="sab-9"></td>
          <td v-bind:class="{ active: estilosHorarios.dom9 }" class="dom-9"></td>
        </tr>
        <tr>
          <th>9:30</th>
          <td v-bind:class="{ active: estilosHorarios.lun93 }" class="lun-9-3"></td>
          <td v-bind:class="{ active: estilosHorarios.mar93 }" class="mar-9-3"></td>
          <td v-bind:class="{ active: estilosHorarios.mie93 }" class="mie-9-3"></td>
          <td v-bind:class="{ active: estilosHorarios.jue93 }" class="jue-9-3"></td>
          <td v-bind:class="{ active: estilosHorarios.vie93 }" class="vie-9-3"></td>
          <td v-bind:class="{ active: estilosHorarios.sab93 }" class="sab-9-3"></td>
          <td v-bind:class="{ active: estilosHorarios.dom93 }" class="dom-9-3"></td>
        </tr>
        <tr>
          <th>10:00</th>
          <td v-bind:class="{ active: estilosHorarios.lun10 }" class="lun-10"></td>
          <td v-bind:class="{ active: estilosHorarios.mar10 }" class="mar-10"></td>
          <td v-bind:class="{ active: estilosHorarios.mie10 }" class="mie-10"></td>
          <td v-bind:class="{ active: estilosHorarios.jue10 }" class="jue-10"></td>
          <td v-bind:class="{ active: estilosHorarios.vie10 }" class="vie-10"></td>
          <td v-bind:class="{ active: estilosHorarios.sab10 }" class="sab-10"></td>
          <td v-bind:class="{ active: estilosHorarios.dom10 }" class="dom-10"></td>
        </tr>
        <tr>
          <th>10:30</th>
          <td v-bind:class="{ active: estilosHorarios.lun103 }" class="lun-10-3"></td>
          <td v-bind:class="{ active: estilosHorarios.mar103 }" class="mar-10-3"></td>
          <td v-bind:class="{ active: estilosHorarios.mie103 }" class="mie-10-3"></td>
          <td v-bind:class="{ active: estilosHorarios.jue103 }" class="jue-10-3"></td>
          <td v-bind:class="{ active: estilosHorarios.vie103 }" class="vie-10-3"></td>
          <td v-bind:class="{ active: estilosHorarios.sab103 }" class="sab-10-3"></td>
          <td v-bind:class="{ active: estilosHorarios.dom103 }" class="dom-10-3"></td>
        </tr>
        <tr>
          <th>11:00</th>
          <td v-bind:class="{ active: estilosHorarios.lun11 }" class="lun-11"></td>
          <td v-bind:class="{ active: estilosHorarios.mar11 }" class="mar-11"></td>
          <td v-bind:class="{ active: estilosHorarios.mie11 }" class="mie-11"></td>
          <td v-bind:class="{ active: estilosHorarios.jue11 }" class="jue-11"></td>
          <td v-bind:class="{ active: estilosHorarios.vie11 }" class="vie-11"></td>
          <td v-bind:class="{ active: estilosHorarios.sab11 }" class="sab-11"></td>
          <td v-bind:class="{ active: estilosHorarios.dom11 }" class="dom-11"></td>
        </tr>
        <tr>
          <th>11:30</th>
          <td v-bind:class="{ active: estilosHorarios.lun113 }" class="lun-11-3"></td>
          <td v-bind:class="{ active: estilosHorarios.mar113 }" class="mar-11-3"></td>
          <td v-bind:class="{ active: estilosHorarios.mie113 }" class="mie-11-3"></td>
          <td v-bind:class="{ active: estilosHorarios.jue113 }" class="jue-11-3"></td>
          <td v-bind:class="{ active: estilosHorarios.vie113 }" class="vie-11-3"></td>
          <td v-bind:class="{ active: estilosHorarios.sab113 }" class="sab-11-3"></td>
          <td v-bind:class="{ active: estilosHorarios.dom113 }" class="dom-11-3"></td>
        </tr>
        <tr>
          <th>12:00</th>
          <td v-bind:class="{ active: estilosHorarios.lun12 }" class="lun-12"></td>
          <td v-bind:class="{ active: estilosHorarios.mar12 }" class="mar-12"></td>
          <td v-bind:class="{ active: estilosHorarios.mie12 }" class="mie-12"></td>
          <td v-bind:class="{ active: estilosHorarios.jue12 }" class="jue-12"></td>
          <td v-bind:class="{ active: estilosHorarios.vie12 }" class="vie-12"></td>
          <td v-bind:class="{ active: estilosHorarios.sab12 }" class="sab-12"></td>
          <td v-bind:class="{ active: estilosHorarios.dom12 }" class="dom-12"></td>
        </tr>
        <tr>
          <th>12:30</th>
          <td v-bind:class="{ active: estilosHorarios.lun123 }" class="lun-12-3"></td>
          <td v-bind:class="{ active: estilosHorarios.mar123 }" class="mar-12-3"></td>
          <td v-bind:class="{ active: estilosHorarios.mie123 }" class="mie-12-3"></td>
          <td v-bind:class="{ active: estilosHorarios.jue123 }" class="jue-12-3"></td>
          <td v-bind:class="{ active: estilosHorarios.vie123 }" class="vie-12-3"></td>
          <td v-bind:class="{ active: estilosHorarios.sab123 }" class="sab-12-3"></td>
          <td v-bind:class="{ active: estilosHorarios.dom123 }" class="dom-12-3"></td>
        </tr>
        <tr>
          <th>13:00</th>
          <td v-bind:class="{ active: estilosHorarios.lun13 }" class="lun-13"></td>
          <td v-bind:class="{ active: estilosHorarios.mar13 }" class="mar-13"></td>
          <td v-bind:class="{ active: estilosHorarios.mie13 }" class="mie-13"></td>
          <td v-bind:class="{ active: estilosHorarios.jue13 }" class="jue-13"></td>
          <td v-bind:class="{ active: estilosHorarios.vie13 }" class="vie-13"></td>
          <td v-bind:class="{ active: estilosHorarios.sab13 }" class="sab-13"></td>
          <td v-bind:class="{ active: estilosHorarios.dom13 }" class="dom-13"></td>
        </tr>
        <tr>
          <th>13:30</th>
          <td v-bind:class="{ active: estilosHorarios.lun133 }" class="lun-13-3"></td>
          <td v-bind:class="{ active: estilosHorarios.mar133 }" class="mar-13-3"></td>
          <td v-bind:class="{ active: estilosHorarios.mie133 }" class="mie-13-3"></td>
          <td v-bind:class="{ active: estilosHorarios.jue133 }" class="jue-13-3"></td>
          <td v-bind:class="{ active: estilosHorarios.vie133 }" class="vie-13-3"></td>
          <td v-bind:class="{ active: estilosHorarios.sab133 }" class="sab-13-3"></td>
          <td v-bind:class="{ active: estilosHorarios.dom133 }" class="dom-13-3"></td>
        </tr>
        <tr>
          <th>14:00</th>
          <td v-bind:class="{ active: estilosHorarios.lun14 }" class="lun-14"></td>
          <td v-bind:class="{ active: estilosHorarios.mar14 }" class="mar-14"></td>
          <td v-bind:class="{ active: estilosHorarios.mie14 }" class="mie-14"></td>
          <td v-bind:class="{ active: estilosHorarios.jue14 }" class="jue-14"></td>
          <td v-bind:class="{ active: estilosHorarios.vie14 }" class="vie-14"></td>
          <td v-bind:class="{ active: estilosHorarios.sab14 }" class="sab-14"></td>
          <td v-bind:class="{ active: estilosHorarios.dom14 }" class="dom-14"></td>
        </tr>
        <tr>
          <th>14:30</th>
          <td v-bind:class="{ active: estilosHorarios.lun143 }" class="lun-14-3"></td>
          <td v-bind:class="{ active: estilosHorarios.mar143 }" class="mar-14-3"></td>
          <td v-bind:class="{ active: estilosHorarios.mie143 }" class="mie-14-3"></td>
          <td v-bind:class="{ active: estilosHorarios.jue143 }" class="jue-14-3"></td>
          <td v-bind:class="{ active: estilosHorarios.vie143 }" class="vie-14-3"></td>
          <td v-bind:class="{ active: estilosHorarios.sab143 }" class="sab-14-3"></td>
          <td v-bind:class="{ active: estilosHorarios.dom143 }" class="dom-14-3"></td>
        </tr>
        <tr>
          <th>15:00</th>
          <td v-bind:class="{ active: estilosHorarios.lun15 }" class="lun-15"></td>
          <td v-bind:class="{ active: estilosHorarios.mar15 }" class="mar-15"></td>
          <td v-bind:class="{ active: estilosHorarios.mie15 }" class="mie-15"></td>
          <td v-bind:class="{ active: estilosHorarios.jue15 }" class="jue-15"></td>
          <td v-bind:class="{ active: estilosHorarios.vie15 }" class="vie-15"></td>
          <td v-bind:class="{ active: estilosHorarios.sab15 }" class="sab-15"></td>
          <td v-bind:class="{ active: estilosHorarios.dom15 }" class="dom-15"></td>
        </tr>
        <tr>
          <th>15:30</th>
          <td v-bind:class="{ active: estilosHorarios.lun153 }" class="lun-15-3"></td>
          <td v-bind:class="{ active: estilosHorarios.mar153 }" class="mar-15-3"></td>
          <td v-bind:class="{ active: estilosHorarios.mie153 }" class="mie-15-3"></td>
          <td v-bind:class="{ active: estilosHorarios.jue153 }" class="jue-15-3"></td>
          <td v-bind:class="{ active: estilosHorarios.vie153 }" class="vie-15-3"></td>
          <td v-bind:class="{ active: estilosHorarios.sab153 }" class="sab-15-3"></td>
          <td v-bind:class="{ active: estilosHorarios.dom153 }" class="dom-15-3"></td>
        </tr>
        <tr>
          <th>16:00</th>
          <td v-bind:class="{ active: estilosHorarios.lun16 }" class="lun-16"></td>
          <td v-bind:class="{ active: estilosHorarios.mar16 }" class="mar-16"></td>
          <td v-bind:class="{ active: estilosHorarios.mie16 }" class="mie-16"></td>
          <td v-bind:class="{ active: estilosHorarios.jue16 }" class="jue-16"></td>
          <td v-bind:class="{ active: estilosHorarios.vie16 }" class="vie-16"></td>
          <td v-bind:class="{ active: estilosHorarios.sab16 }" class="sab-16"></td>
          <td v-bind:class="{ active: estilosHorarios.dom16 }" class="dom-16"></td>
        </tr>
        <tr>
          <th>16:30</th>
          <td v-bind:class="{ active: estilosHorarios.lun163 }" class="lun-16-3"></td>
          <td v-bind:class="{ active: estilosHorarios.mar163 }" class="mar-16-3"></td>
          <td v-bind:class="{ active: estilosHorarios.mie163 }" class="mie-16-3"></td>
          <td v-bind:class="{ active: estilosHorarios.jue163 }" class="jue-16-3"></td>
          <td v-bind:class="{ active: estilosHorarios.vie163 }" class="vie-16-3"></td>
          <td v-bind:class="{ active: estilosHorarios.sab163 }" class="sab-16-3"></td>
          <td v-bind:class="{ active: estilosHorarios.dom163 }" class="dom-16-3"></td>
        </tr>
        <tr>
          <th>17:00</th>
          <td v-bind:class="{ active: estilosHorarios.lun17 }" class="lun-17"></td>
          <td v-bind:class="{ active: estilosHorarios.mar17 }" class="mar-17"></td>
          <td v-bind:class="{ active: estilosHorarios.mie17 }" class="mie-17"></td>
          <td v-bind:class="{ active: estilosHorarios.jue17 }" class="jue-17"></td>
          <td v-bind:class="{ active: estilosHorarios.vie17 }" class="vie-17"></td>
          <td v-bind:class="{ active: estilosHorarios.sab17 }" class="sab-17"></td>
          <td v-bind:class="{ active: estilosHorarios.dom17 }" class="dom-17"></td>
        </tr>
        <tr>
          <th>17:30</th>
          <td v-bind:class="{ active: estilosHorarios.lun173 }" class="lun-17-3"></td>
          <td v-bind:class="{ active: estilosHorarios.mar173 }" class="mar-17-3"></td>
          <td v-bind:class="{ active: estilosHorarios.mie173 }" class="mie-17-3"></td>
          <td v-bind:class="{ active: estilosHorarios.jue173 }" class="jue-17-3"></td>
          <td v-bind:class="{ active: estilosHorarios.vie173 }" class="vie-17-3"></td>
          <td v-bind:class="{ active: estilosHorarios.sab173 }" class="sab-17-3"></td>
          <td v-bind:class="{ active: estilosHorarios.dom173 }" class="dom-17-3"></td>
        </tr>
        <tr>
          <th>18:00</th>
          <td v-bind:class="{ active: estilosHorarios.lun18 }" class="lun-18"></td>
          <td v-bind:class="{ active: estilosHorarios.mar18 }" class="mar-18"></td>
          <td v-bind:class="{ active: estilosHorarios.mie18 }" class="mie-18"></td>
          <td v-bind:class="{ active: estilosHorarios.jue18 }" class="jue-18"></td>
          <td v-bind:class="{ active: estilosHorarios.vie18 }" class="vie-18"></td>
          <td v-bind:class="{ active: estilosHorarios.sab18 }" class="sab-18"></td>
          <td v-bind:class="{ active: estilosHorarios.dom18 }" class="dom-18"></td>
        </tr>
        <tr>
          <th>18:30</th>
          <td v-bind:class="{ active: estilosHorarios.lun183 }" class="lun-18-3"></td>
          <td v-bind:class="{ active: estilosHorarios.mar183 }" class="mar-18-3"></td>
          <td v-bind:class="{ active: estilosHorarios.mie183 }" class="mie-18-3"></td>
          <td v-bind:class="{ active: estilosHorarios.jue183 }" class="jue-18-3"></td>
          <td v-bind:class="{ active: estilosHorarios.vie183 }" class="vie-18-3"></td>
          <td v-bind:class="{ active: estilosHorarios.sab183 }" class="sab-18-3"></td>
          <td v-bind:class="{ active: estilosHorarios.dom183 }" class="dom-18-3"></td>
        </tr>
        <tr>
          <th>19:00</th>
          <td v-bind:class="{ active: estilosHorarios.lun19 }" class="lun-19"></td>
          <td v-bind:class="{ active: estilosHorarios.mar19 }" class="mar-19"></td>
          <td v-bind:class="{ active: estilosHorarios.mie19 }" class="mie-19"></td>
          <td v-bind:class="{ active: estilosHorarios.jue19 }" class="jue-19"></td>
          <td v-bind:class="{ active: estilosHorarios.vie19 }" class="vie-19"></td>
          <td v-bind:class="{ active: estilosHorarios.sab19 }" class="sab-19"></td>
          <td v-bind:class="{ active: estilosHorarios.dom19 }" class="dom-19"></td>
        </tr>
        <tr>
          <th>19:30</th>
          <td v-bind:class="{ active: estilosHorarios.lun193 }" class="lun-19-3"></td>
          <td v-bind:class="{ active: estilosHorarios.mar193 }" class="mar-19-3"></td>
          <td v-bind:class="{ active: estilosHorarios.mie193 }" class="mie-19-3"></td>
          <td v-bind:class="{ active: estilosHorarios.jue193 }" class="jue-19-3"></td>
          <td v-bind:class="{ active: estilosHorarios.vie193 }" class="vie-19-3"></td>
          <td v-bind:class="{ active: estilosHorarios.sab193 }" class="sab-19-3"></td>
          <td v-bind:class="{ active: estilosHorarios.dom193 }" class="dom-19-3"></td>
        </tr>
        <tr>
          <th>20:00</th>
          <td v-bind:class="{ active: estilosHorarios.lun20 }" class="lun-20"></td>
          <td v-bind:class="{ active: estilosHorarios.mar20 }" class="mar-20"></td>
          <td v-bind:class="{ active: estilosHorarios.mie20 }" class="mie-20"></td>
          <td v-bind:class="{ active: estilosHorarios.jue20 }" class="jue-20"></td>
          <td v-bind:class="{ active: estilosHorarios.vie20 }" class="vie-20"></td>
          <td v-bind:class="{ active: estilosHorarios.sab20 }" class="sab-20"></td>
          <td v-bind:class="{ active: estilosHorarios.dom20 }" class="dom-20"></td>
        </tr>
      </mdb-tbl-body>
    </mdb-tbl>
  </div>
</template>

<script lang="ts">
import Vue from 'vue';
import { Component, Prop } from 'vue-property-decorator';
import { mdbTbl, mdbTblHead, mdbTblBody, mdbBtn } from 'mdbvue';

const fechaFormateada = {
  dia: '',
  horarioInicial: '',
  horarioFinal: '',
};

const estilosHorarioFormateado: any = {
    lun6: false,
    mar6: false,
    mie6: false,
    jue6: false,
    vie6: false,
    sab6: false,
    dom6: false,
    lun63: false,
    mar63: false,
    mie63: false,
    jue63: false,
    vie63: false,
    sab63: false,
    dom63: false,
    lun7: true,
    mar7: false,
    mie7: false,
    jue7: false,
    vie7: false,
    sab7: false,
    dom7: false,
    lun73: true,
    mar73: false,
    mie73: false,
    jue73: false,
    vie73: false,
    sab73: false,
    dom73: false,
    lun8: true,
    mar8: false,
    mie8: false,
    jue8: false,
    vie8: false,
    sab8: false,
    dom8: false,
    lun83: false,
    mar83: false,
    mie83: false,
    jue83: false,
    vie83: false,
    sab83: false,
    dom83: false,
    lun9: false,
    mar9: false,
    mie9: false,
    jue9: false,
    vie9: false,
    sab9: false,
    dom9: false,
    lun93: false,
    mar93: false,
    mie93: false,
    jue93: false,
    vie93: false,
    sab93: false,
    dom93: false,
    lun10: false,
    mar10: false,
    mie10: false,
    jue10: false,
    vie10: false,
    sab10: false,
    dom10: false,
    lun103: false,
    mar103: false,
    mie103: false,
    jue103: false,
    vie103: false,
    sab103: false,
    dom103: false,
    lun11: false,
    mar11: false,
    mie11: false,
    jue11: false,
    vie11: false,
    sab11: false,
    dom11: false,
    lun113: false,
    mar113: false,
    mie113: false,
    jue113: false,
    vie113: false,
    sab113: false,
    dom113: false,
    lun12: false,
    mar12: false,
    mie12: false,
    jue12: false,
    vie12: false,
    sab12: false,
    dom12: false,
    lun123: false,
    mar123: false,
    mie123: false,
    jue123: false,
    vie123: false,
    sab123: false,
    dom123: false,
    lun13: false,
    mar13: false,
    mie13: false,
    jue13: false,
    vie13: false,
    sab13: false,
    dom13: false,
    lun133: false,
    mar133: false,
    mie133: false,
    jue133: false,
    vie133: false,
    sab133: false,
    dom133: false,
    lun14: false,
    mar14: false,
    mie14: false,
    jue14: false,
    vie14: false,
    sab14: false,
    dom14: false,
    lun143: false,
    mar143: false,
    mie143: false,
    jue143: false,
    vie143: false,
    sab143: false,
    dom143: false,
    lun15: false,
    mar15: false,
    mie15: false,
    jue15: false,
    vie15: false,
    sab15: false,
    dom15: false,
    lun153: false,
    mar153: false,
    mie153: false,
    jue153: false,
    vie153: false,
    sab153: false,
    dom153: false,
    lun16: false,
    mar16: false,
    mie16: false,
    jue16: false,
    vie16: false,
    sab16: false,
    dom16: false,
    lun163: false,
    mar163: false,
    mie163: false,
    jue163: false,
    vie163: false,
    sab163: false,
    dom163: false,
    lun17: false,
    mar17: false,
    mie17: false,
    jue17: false,
    vie17: false,
    sab17: false,
    dom17: false,
    lun173: false,
    mar173: false,
    mie173: false,
    jue173: false,
    vie173: false,
    sab173: false,
    dom173: false,
    lun18: false,
    mar18: false,
    mie18: false,
    jue18: false,
    vie18: false,
    sab18: false,
    dom18: false,
    lun183: false,
    mar183: false,
    mie183: false,
    jue183: false,
    vie183: false,
    sab183: false,
    dom183: false,
    lun19: false,
    mar19: false,
    mie19: false,
    jue19: false,
    vie19: false,
    sab19: false,
    dom19: false,
    lun193: false,
    mar193: false,
    mie193: false,
    jue193: false,
    vie193: false,
    sab193: false,
    dom193: false,
    lun20: false,
    mar20: false,
    mie20: false,
    jue20: false,
    vie20: false,
    sab20: false,
    dom20: false,
};

@Component({
  name: 'HelloWorld',
  components: {
    mdbTbl,
    mdbTblHead,
    mdbTblBody,
    mdbBtn,
  },
})
export default class HelloWorld extends Vue {

  public fecha = {
    ...fechaFormateada,
  };

  public estilosHorarios: any = {
    ...estilosHorarioFormateado,
  };

  private fechas = [
    {
      dia: 'lun',
      horarioInicial: '7',
      horarioFinal: '8',
    },
  ];

  private horarios = [
    '6',
    '6-3',
    '7',
    '7-3',
    '8',
    '8-3',
    '9',
    '9-3',
    '10',
    '10-3',
    '11',
    '11-3',
    '12',
    '12-3',
    '13',
    '13-3',
    '14',
    '14-3',
    '15',
    '15-3',
    '16',
    '16-3',
    '17',
    '17-3',
    '18',
    '18-3',
    '19',
    '19-3',
    '20',
  ];

  private checkNuevaFecha = false;
  private errorAndBreak = false;

  constructor() {
    super();
  }

  public crearHorario(): void {
    if (this.fecha.dia.length === 0 && this.fecha.horarioInicial.length === 0 && this.fecha.horarioFinal.length === 0) {
      alert('Complete los datos');
    } else {
      this.errorAndBreak = false;
      this.fechas.forEach((fechaGuardada) => {
        if (fechaGuardada.dia === this.fecha.dia && !this.errorAndBreak) {
          console.log('fechaGuardada.dia', fechaGuardada.dia);
          console.log('this.fecha.dia', this.fecha.dia);
          this.checkNuevaFecha = false;
          const space = this.horarios.findIndex((horario) => horario === fechaGuardada.horarioInicial);
          const newSpace = this.horarios.findIndex((horario) => horario === this.fecha.horarioInicial);
          const spaceTwo = this.horarios.findIndex((horario) => horario === fechaGuardada.horarioFinal);
          const newSpaceTwo = this.horarios.findIndex((horario) => horario === this.fecha.horarioFinal);
          if (newSpace > newSpaceTwo) {
            this.errorAndBreak = true;
            alert('Ingrese un horario correcto');
          } else {
            if (newSpace >= space && newSpace <= spaceTwo) {
              this.errorAndBreak = true;
              alert('El horario inicial no se puede sobreponer');
            } else {
              if (newSpaceTwo <= spaceTwo && newSpaceTwo >= space) {
                this.errorAndBreak = true;
                alert('El horario final no se puede sobreponer');
              } else {
                if (newSpace <= space && newSpaceTwo >= spaceTwo) {
                  this.errorAndBreak = true;
                  alert('Los horarios están dentro de un horario ya asignado');
                } else {
                  this.pintarHorario();
                }
              }
            }
          }
        } else {
          this.checkNuevaFecha = true;
        }
      });
      if (this.checkNuevaFecha) {
        console.log('Guardar nueva fecha y pintarla');
        this.pintarHorario();
      }
    }
  }

  private pintarHorario() {
    const inicio = this.horarios.findIndex((horario) => horario === this.fecha.horarioInicial);
    const fin = this.horarios.findIndex((horario) => horario === this.fecha.horarioFinal);
    for (let i = inicio; i <= fin; i++) {
      const campo = this.fecha.dia + this.horarios[i].replace('-', '');
      console.log(campo);
      this.estilosHorarios[campo] = true;
    }
    console.log(this.fecha);
    this.fechas.push(this.fecha);
    this.fecha = {
      ...fechaFormateada,
    };
  }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
.active {
  background-color: #42b983;
}
</style>
