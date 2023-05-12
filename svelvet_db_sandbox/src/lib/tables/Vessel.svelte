<script>
  import {Node, Anchor} from 'svelvet';
</script>
<!-- bgColor='#fae8e8' -->
<Node useDefaults id='vessel' position={{x:200, y:20}}>
  <div class="nodeWrapper">
    <div class='inputAnchor'>
      <Anchor id='vesselAnchor' input></Anchor>
    </div>
    <div id='container'>
      <div id='heading'>Vessels</div>
      <table id="vesselTable">
          <tr>
              <td>id</td>
              <td>bigint</td>
              <td>autoincrement()</td>
          </tr>
          <tr>
              <td>name</td>
              <td>varchar</td>
              <td></td>
          </tr>
          <tr>
              <td>manufacturer</td>
              <td>varchar</td>
              <td></td>
          </tr>
        <tr>
          <td>model</td>
          <td>varchar</td>
          <td></td>
        </tr>
        <tr>
          <td>vessel_type</td>
          <td>varchar</td>
          <td></td>
        </tr>
        <tr>
          <td>vessel_class</td>
          <td>varchar</td>
          <td></td>
        </tr>
        <tr>
          <td>cost_in_credits</td>
          <td>bigint</td>
          <td></td>
        </tr>
        <tr>
          <td>length</td>
          <td>varchar</td>
          <td></td>
        </tr>
        <tr>
          <td>max_atmosphering_speed</td>
          <td>varchar</td>
          <td></td>
        </tr>
        <tr>
          <td>crew</td>
          <td>int</td>
          <td></td>
        </tr>
        <tr>
          <td>passengers</td>
          <td>int</td>
          <td></td>
        </tr>
        <tr>
          <td>cargo_capacity</td>
          <td>varchar</td>
          <td></td>
        </tr>
        <tr>
          <td>consumables</td>
          <td>varchar</td>
          <td></td>
        </tr>
      </table>
    </div>
    <div class='outputAnchor'>
      <Anchor connections={[['people','peopleAnchor']]} output></Anchor>
    </div> 
  </div>
</Node>


<style>

.nodeWrapper{
  box-sizing: border-box;
  width:fit-content;
  border-radius: 8px;
  height: fit-content;
  position: relative;
  pointer-events: auto;
  display: flex;
  flex-direction: column;
  padding: 1px;
  gap: 10px;
}

.inputAnchor{
        position: absolute;
        display: flex;
        flex-direction: column;
        gap: 10px;
        top: 50px;
        left: -16px;
}

.outputAnchor{
        position: absolute;
        display: flex;
        flex-direction: column;
        gap: 10px;
        top: 50px;
        right: -14px;
}

#heading{
        display: flex;
        justify-content: center;
        background-color: lightblue;
        border-top-right-radius: 8px;
        border-top-left-radius: 8px;
        padding: 10px;
        font-size: 18px;
        font-weight: 600;
    }
    
  #vesselTable td{
        width: 70px;
        margin: 0px;
        padding: 8px;
        justify-content: space-evenly;
        border-bottom: 1px solid gray;
        border-right: 1px solid gray;
  }

  #vesselTable td:last-child {       
        border-right: none;
    }
</style>