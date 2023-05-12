<script>
    import {Node, Anchor} from 'svelvet';
  </script>
  <!-- bgColor='#dff7df' -->
  <Node  useDefaults id='starship' position={{x:5, y:5}}>
    <div class='nodeWrapper'>
    <div id='container'>
      <div id='heading'>Starship Specs</div>
      <table id="starshipTable">
          <tr>
              <td>id</td>
              <td>bigint</td> 
              <td>autoincrement()</td>     
          </tr>
          <tr>
             <td>hyperdrive_rating</td>
             <td>varchar</td> 
             <td></td>  
          </tr>
          <tr>
            <td>MGLT</td>
            <td>varchar</td> 
            <td></td>  
         </tr>
         <tr>
            <td>vessel_id</td>
            <td>bigint</td> 
            <td></td>  
         </tr>
      </table>
    </div>
    <div class='outputAnchor'>
    <Anchor connections={[['user', 'userAnchor']]} output></Anchor>
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

.outputAnchor{
        position: absolute;
        display: flex;
        flex-direction: column;
        gap: 10px;
        bottom: -14px;
        left: 36px;
    }
  
  #heading{
          display: flex;
          justify-content: center;
          background-color: lightblue;
          padding: 10px;
          font-size: 18px;
          font-weight: 600;
          border-top-right-radius: 8px;
          border-top-left-radius: 8px;
      }
      
    #starshipTable td{
        width: 70px;
          margin: 0px;
          padding: 8px;
          justify-content: space-evenly;
          border-bottom: 1px solid gray;
          border-right: 1px solid gray;
    }
  
    #starshipTable td:last-child {       
          border-right: none;
      }
  </style>