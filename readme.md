Arama ve Çoklu seçim özellikli dropdown list.

jquery-1.12.4.min.js gerektir !

HTML :

    <div class="dropdown">
        <select style="display:none" name="" id="secimler" multiple> </select>
    </div>
    
JS : 

    let data = [
      {id: 1,name: "Seçim 1",selected:true},
      {id: 2,name: "Seçim 2",selected:false},
      {id: 3,name: "Seçim 3",selected:false},
    ]

    $('.dropdown').dropdown({
        input: '<input type="text" maxLength="20" placeholder="Bir seçim yapınız ...">',
        data: data,
        limitCount: 10,
        multipleMode: 'label',
        choice: function () {
          console.log($('#secimler').val())
        }
    });
