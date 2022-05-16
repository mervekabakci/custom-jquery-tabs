# custom-jquery-tabs

jQuery tab örneğinde iç içe tablar, aynı sayfada birden fazla tab ekleyebilir ve özelleştirebilirsiniz. 

jQuery tab menü için https://code.jquery.com/jquery-3.6.0.min.js kodunu yazacağınız script kodunuzun üst kısmına ekleyiniz.

Örneğin;

    <script type="text/javascript" language="javascript" src="jquery-3.6.0.min.js"></script>
    <script type="text/javascript" language="javascript">
        var subcontentTab = $(".tabContent").children(".tabsContent");
        subcontentTab.parent().addClass("submain");

        $(".tabsTitle > .tabButton").click(function () {
            var elemnt = $(this),
                indis = $(this).index(),
                parentelemnt = elemnt.parent(),
                elemntchild = parentelemnt.children();
                elemntmain = parentelemnt.parent(),
                content = elemntmain.children(".tabsContent"),
                contentelemnt = content.children(),
                submain = contentelemnt.parents(".tabContent"),
                subcontent = submain.children(".tabsContent"),
                subcontentelemnt = subcontent.children();
                
                elemntchild.removeClass("active");
                contentelemnt.removeClass("active");

                elemnt.addClass("active");

                if(elemntmain.hasClass("myTabs")){
                    elemntmain.addClass("maintabs");
                }

                contentelemnt.eq(indis).addClass("active");
        });
    </script>


  Html Kodu  
            
    <div class="myTabs">
        <div class="tabsTitle">
            <a class="tabButton active">Tab 1</a>
            <a class="tabButton">Tab 2</a>
            <a class="tabButton">Tab 3</a>
        </div>
        <div class="tabsContent">
            <div class="tabContent active">
                <h2>tab Content 1</h2>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Repellat similique saepe pariatur praesentium vitae natus autem quae ex, corrupti </p>
            </div>
            <div class="tabContent">
                <div class="tabsTitle">
                    <a class="tabButton">Tab 2-1</a>
                    <a class="tabButton active">Tab 2-2</a>
                    <a class="tabButton">Tab 2-3</a>
                </div>
                <div class="tabsContent">
                    <div class="tabContent">
                        <h2>tab Content 2-1</h2>
                        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Repellat similique saepe pariatur praesentium</p>
                    </div>
                    <div class="tabContent active">
                        <h2>tab Content 2-2</h2>
                        <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Iusto eveniet voluptatibus libero dignissimos maxime? Quia</p>
                    </div>
                    <div class="tabContent">
                        <div class="tabsTitle">
                            <a class="tabButton">Tab 2-1</a>
                            <a class="tabButton active">Tab 2-2</a>
                            <a class="tabButton">Tab 2-3</a>
                        </div>
                        <div class="tabsContent">
                            <div class="tabContent">
                                <h2>tab Content 2-1</h2>
                                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Repellat similique saepe pariatur praesentium vitae </p>
                            </div>
                            <div class="tabContent active">
                                <h2>tab Content 2-2</h2>
                                <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Iusto eveniet voluptatibus libero dignissimos maxime? Quia debitis</p>
                            </div>
                            <div class="tabContent">
                                <h2>tab Content 2-3</h2>
                                <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Dolor consequatur, saepe magnam delectus nesciunt officiis vero libero</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <div class="tabContent">
                <h2>tab Content 3</h2>
                <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Dolor consequatur, saepe magnam delectus nesciunt officiis vero libero volup</p>
            </div>
        </div>
    </div> 
    
    
 Css kodu
 
     <style type="text/css">
        body{
            margin:0;
            background-color:#aa9f9f;
        }
        .myTabs{
            margin:25px auto;
            max-width: 80%;
        }
        .myTabs .tabsContent{
            width: 100%;
        }
        .myTabs .tabsTitle{
            display: flex;
            flex-wrap: wrap;
        }
        .myTabs .tabsTitle .tabButton{
            padding:25px;
            background-color:#838181;
            color:#ffffff;
            font-family: Arial, Helvetica, sans-serif;
            font-size:16px;
            border-left:1px solid lightgray;
            flex:1;
            cursor: pointer;
            transition: all .3s ease-in-out;
        }
        .myTabs .tabsTitle .tabButton:hover{
            background-color:#5a5858;
        }
        .myTabs .tabsTitle .tabButton.active{
            background-color:#ffffff;
            color:#5a5858;
            font-weight: bold;
        }
        .myTabs .tabsTitle .tabButton:first-child{
            border-left:none;
        }
        .myTabs .tabsContent .tabContent{
            background-color:#ffffff;
            padding:25px;
            font-family: Arial, Helvetica, sans-serif;
            font-size:12px;
            display: none;
        }
        .myTabs .tabsContent .tabContent h2{
            font-family: Arial, Helvetica, sans-serif;
        }

        .myTabs .tabsContent .tabContent.active{
            display: block;
        }
        
        .myTabs .tabsContent .tabContent.submain{
            padding:10px 0 0;
        }
        .myTabs .tabsContent .tabContent.submain .tabsTitle{
            width: 98%;
            margin:10px auto;
            
        }
        .myTabs .tabsContent .tabContent.submain .tabsTitle .tabButton{
            background-color:brown;
            border-top:1px solid #d47979;
        }
        .myTabs .tabsContent .tabContent.submain .tabsTitle .tabButton.active{
            background-color:#d47979;
            color:brown;
        }
        .myTabs .tabsContent .tabContent.submain .tabsTitle .tabButton:hover{
            background-color:#d47979;
        }
    </style>
