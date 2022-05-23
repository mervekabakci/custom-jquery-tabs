# custom-jquery-tabs

jQuery tab örneğinde iç içe tablar, aynı sayfada birden fazla tab ekleyebilir ve özelleştirebilirsiniz. 
Aşağıdaki kod yapısı 06-js-jquery-library-nested-tab.html sayfasını ve farklı jQuery örneklerni klasör içerisindeki html sayfalardan inceleyebilirsiniz.

jQuery tab menü için https://code.jquery.com/jquery-3.6.0.min.js kodunu yazacağınız script kodunuzun üst kısmına ekleyiniz.

Örneğin;

    <script type="text/javascript" language="javascript" src="jquery-3.6.0.min.js"></script>
    <script type="text/javascript" language="javascript">
        $(".tabContent").children(".tabsContent").parent().addClass("submain");

        $(".tabsTitle > .tabButton").click(function () {
            var $elemnt = $(this),
                $indis = $(this).index(),
                $tab = $elemnt.siblings(),
                $content = $tab.parent().siblings().children();

                $tab.removeClass("active");
                $elemnt.addClass("active");

                $content.removeClass("active");
                $content.eq($indis).addClass("active");
        });
    </script>


  Html Kodu  
            
    <div class="center">
        <div class="myTabs">
            <div class="tabsTitle">
                <a class="tabButton active">Tab 1</a>
                <a class="tabButton">Tab 2</a>
                <a class="tabButton">Tab 3</a>
            </div>
            <div class="tabsContent">
                <div class="tabContent active">
                    <h2>tab Content 1</h2>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Repellat similique saepe pariatur praesentium vitae natus autem quae ex, corrupti numquam non, id labore! Dolore, corrupti adipisci natus placeat eligendi vitae tenetur, modi in ipsa laboriosam magni laborum delectus nemo quibusdam mollitia minima. Ut fugiat assumenda placeat? Ipsum voluptas vel itaque animi nisi velit, at explicabo et numquam vitae, ex neque magnam, quasi eligendi? Provident cupiditate maiores labore ducimus reprehenderit incidunt omnis iure pariatur veniam optio aliquam, non similique fugiat deserunt, beatae expedita est voluptatum aut hic. Distinctio, perspiciatis voluptates? Saepe impedit aliquid, reprehenderit dolor explicabo sit nemo cum vel cupiditate quia doloribus rerum veniam minima nulla velit doloremque, error a autem inventore facere expedita totam amet quisquam. A dolor est assumenda labore sit quia repellendus ut iure architecto? Enim reiciendis ipsam, a quae ipsum consequuntur adipisci iste incidunt provident excepturi sit porro eveniet libero molestias tempora consequatur quibusdam! Aliquid consectetur sequi dolores illum voluptatibus, impedit temporibus consequatur fugit! Delectus, et. Eum ipsum doloremque perspiciatis eligendi recusandae earum officiis! Laborum alias quam labore voluptate minima repellendus illo molestias praesentium consectetur possimus, hic soluta iure velit omnis, amet impedit. Ipsa, placeat minus voluptate consectetur quisquam magnam! Doloribus illo pariatur provident mollitia facilis!</p>
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
                                <p>Lorem ipsum dolor, id labore! Dolore, corrupti adipisci natus placeat eligendi vitae tenetur, modi in ipsa laboriosam magni laborum delectus nemo quibusdam mollitia minima. Ut fugiat assumenda placeat? Ipsum voluptas vel itaque animi nisi velit, at explicabo et numquam vitae, ex neque magnam, quasi eligendi? Provident cupiditate maiores labore ducimus reprehenderit incidunt omnis iure pariatur veniam optio aliquam, non similique fugiat deserunt, beatae expedita est voluptatum aut hic. Distinctio, perspiciatis voluptates? Saepe impedit aliquid, reprehenderit dolor explicabo sit nemo cum vel cupiditate quia doloribus rerum veniam minima nulla velit doloremque, error a autem inventore facere expedita totam amet quisquam. A dolor est assumenda labore sit quia repellendus ut iure architecto? Enim reiciendis ipsam, a quae ipsum consequuntur adipisci iste incidunt provident excepturi sit porro eveniet libero molestias tempora consequatur quibusdam! Aliquid consectetur sequi dolores illum voluptatibus, impedit temporibus consequatur fugit! Delectus, et. Eum ipsum doloremque perspiciatis eligendi recusandae earum officiis! Laborum alias quam labore voluptate minima repellendus illo molestias praesentium consectetur possimus, hic soluta iure velit omnis, amet impedit. Ipsa, placeat minus voluptate consectetur quisquam magnam! Doloribus illo pariatur provident mollitia facilis!</p>
                            </div>
                            <div class="tabContent active">
                                <h2>tab Content 2-2</h2>
                                <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Iusto eveniet voluptatibus libero dignissimos maxime? Quia debitis aperiam nemo ea officia accusamus sint fugiat natus itaque esse facere perferendis hic minima cumque quidem iusto, earum deserunt suscipit sit! Suscipit nisi, ipsum fuga excepturi cumque mollitia quos, nesciunt rem fugiat quo voluptate?</p>
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
                                            <p>sub tab 2-1</p>
                                        </div>
                                        <div class="tabContent active">
                                            <h2>tab Content 2-2</h2>
                                            <p>sub tab 2-2</p>
                                        </div>
                                        <div class="tabContent">
                                            <h2>tab Content 2-3</h2>
                                            <p>sub tab 2-3</p>
                                        </div>
                                    </div>
                            </div>
                        </div>
                </div>
                <div class="tabContent">
                    <h2>tab Content 3</h2>
                    <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Dolor consequatur, saepe magnam delectus nesciunt officiis vero libero voluptates debitis sint quisquam earum aliquid velit eum impedit! Minima quibusdam a, voluptatum ullam blanditiis harum sed ipsum temporibus delectus soluta ad cum aliquid tenetur quia sapiente asperiores numquam nihil at sunt distinctio. Labore asperiores eaque sequi exercitationem nam possimus, suscipit in corporis vero pariatur consequuntur explicabo nesciunt deleniti odit, officia quod reprehenderit.</p>
                </div>
            </div>
        </div>

        <div class="myTabs">
            <div class="tabsTitle">
                <a class="tabButton active">Tab 1</a>
                <a class="tabButton">Tab 2</a>
                <a class="tabButton">Tab 3</a>
            </div>
            <div class="tabsContent">
                <div class="tabContent active">
                    <h2>tab Content 1</h2>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Repellat similique saepe pariatur praesentium vitae natus autem quae ex, corrupti numquam non, id labore! Dolore, corrupti adipisci natus placeat eligendi vitae tenetur, modi in ipsa laboriosam magni laborum delectus nemo quibusdam mollitia minima. Ut fugiat assumenda placeat? Ipsum voluptas vel itaque animi nisi velit, at explicabo et numquam vitae, ex neque magnam, quasi eligendi? Provident cupiditate maiores labore ducimus reprehenderit incidunt omnis iure pariatur veniam optio aliquam, non similique fugiat deserunt, beatae expedita est voluptatum aut hic. Distinctio, perspiciatis voluptates? Saepe impedit aliquid, reprehenderit dolor explicabo sit nemo cum vel cupiditate quia doloribus rerum veniam minima nulla velit doloremque, error a autem inventore facere expedita totam amet quisquam. A dolor est assumenda labore sit quia repellendus ut iure architecto? Enim reiciendis ipsam, a quae ipsum consequuntur adipisci iste incidunt provident excepturi sit porro eveniet libero molestias tempora consequatur quibusdam! Aliquid consectetur sequi dolores illum voluptatibus, impedit temporibus consequatur fugit! Delectus, et. Eum ipsum doloremque perspiciatis eligendi recusandae earum officiis! Laborum alias quam labore voluptate minima repellendus illo molestias praesentium consectetur possimus, hic soluta iure velit omnis, amet impedit. Ipsa, placeat minus voluptate consectetur quisquam magnam! Doloribus illo pariatur provident mollitia facilis!</p>
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
                                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Repellat similique saepe pariatur praesentium vitae natus autem quae ex, corrupti numquam non, id labore! Dolore, corrupti adipisci natus placeat eligendi vitae tenetur, modi in ipsa laboriosam magni laborum delectus nemo quibusdam mollitia minima. Ut fugiat assumenda placeat? Ipsum voluptas vel itaque animi nisi velit, at explicabo et numquam vitae, ex neque magnam, quasi eligendi? Provident cupiditate maiores labore ducimus reprehenderit incidunt omnis iure pariatur veniam optio aliquam, non similique fugiat deserunt, beatae expedita est voluptatum aut hic. Distinctio, perspiciatis voluptates? Saepe impedit aliquid, reprehenderit dolor explicabo sit nemo cum vel cupiditate quia doloribus rerum veniam minima nulla velit doloremque, error a autem inventore facere expedita totam amet quisquam. A dolor est assumenda labore sit quia repellendus ut iure architecto? Enim reiciendis ipsam, a quae ipsum consequuntur adipisci iste incidunt provident excepturi sit porro eveniet libero molestias tempora consequatur quibusdam! Aliquid consectetur sequi dolores illum voluptatibus, impedit temporibus consequatur fugit! Delectus, et. Eum ipsum doloremque perspiciatis eligendi recusandae earum officiis! Laborum alias quam labore voluptate minima repellendus illo molestias praesentium consectetur possimus, hic soluta iure velit omnis, amet impedit. Ipsa, placeat minus voluptate consectetur quisquam magnam! Doloribus illo pariatur provident mollitia facilis!</p>
                            </div>
                            <div class="tabContent active">
                                <h2>tab Content 2-2</h2>
                                <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Iusto eveniet voluptatibus libero dignissimos maxime? Quia debitis aperiam nemo ea officia accusamus sint fugiat natus itaque esse facere perferendis hic minima cumque quidem iusto, earum deserunt suscipit sit! Suscipit nisi, ipsum fuga excepturi cumque mollitia quos, nesciunt rem fugiat quo voluptate?</p>
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
                                            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Repellat similique saepe pariatur praesentium vitae natus autem quae ex, corrupti numquam non, id labore! Dolore, corrupti adipisci natus placeat eligendi vitae tenetur, modi in ipsa laboriosam magni laborum delectus nemo quibusdam mollitia minima. Ut fugiat assumenda placeat? Ipsum voluptas vel itaque animi nisi velit, at explicabo et numquam vitae, ex neque magnam, quasi eligendi? Provident cupiditate maiores labore ducimus reprehenderit incidunt omnis iure pariatur veniam optio aliquam, non similique fugiat deserunt, beatae expedita est voluptatum aut hic. Distinctio, perspiciatis voluptates? Saepe impedit aliquid, reprehenderit dolor explicabo sit nemo cum vel cupiditate quia doloribus rerum veniam minima nulla velit doloremque, error a autem inventore facere expedita totam amet quisquam. A dolor est assumenda labore sit quia repellendus ut iure architecto? Enim reiciendis ipsam, a quae ipsum consequuntur adipisci iste incidunt provident excepturi sit porro eveniet libero molestias tempora consequatur quibusdam! Aliquid consectetur sequi dolores illum voluptatibus, impedit temporibus consequatur fugit! Delectus, et. Eum ipsum doloremque perspiciatis eligendi recusandae earum officiis! Laborum alias quam labore voluptate minima repellendus illo molestias praesentium consectetur possimus, hic soluta iure velit omnis, amet impedit. Ipsa, placeat minus voluptate consectetur quisquam magnam! Doloribus illo pariatur provident mollitia facilis!</p>
                                        </div>
                                        <div class="tabContent active">
                                            <h2>tab Content 2-2</h2>
                                            <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Iusto eveniet voluptatibus libero dignissimos maxime? Quia debitis aperiam nemo ea officia accusamus sint fugiat natus itaque esse facere perferendis hic minima cumque quidem iusto, earum deserunt suscipit sit! Suscipit nisi, ipsum fuga excepturi cumque mollitia quos, nesciunt rem fugiat quo voluptate?</p>
                                        </div>
                                        <div class="tabContent">
                                            <h2>tab Content 2-3</h2>
                                            <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Dolor consequatur, saepe magnam delectus nesciunt officiis vero libero voluptates debitis sint quisquam earum aliquid velit eum impedit! Minima quibusdam a, voluptatum ullam blanditiis harum sed ipsum temporibus delectus soluta ad cum aliquid tenetur quia sapiente asperiores numquam nihil at sunt distinctio. Labore asperiores eaque sequi exercitationem nam possimus, suscipit in corporis vero pariatur consequuntur explicabo nesciunt deleniti odit, officia quod reprehenderit.</p>
                                        </div>
                                    </div>
                            </div>
                        </div>
                </div>
                <div class="tabContent">
                    <h2>tab Content 3</h2>
                    <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Dolor consequatur, saepe magnam delectus nesciunt officiis vero libero voluptates debitis sint quisquam earum aliquid velit eum impedit! Minima quibusdam a, voluptatum ullam blanditiis harum sed ipsum temporibus delectus soluta ad cum aliquid tenetur quia sapiente asperiores numquam nihil at sunt distinctio. Labore asperiores eaque sequi exercitationem nam possimus, suscipit in corporis vero pariatur consequuntur explicabo nesciunt deleniti odit, officia quod reprehenderit.</p>
                </div>
            </div>
        </div>
    </div>
    
    
 Css kodu
 
     <style type="text/css">
       body{
            margin:0;
            background-color:#aa9f9f;
        }
        .center{
            margin:0 auto;
            display:flex;
            width: 100%;
            justify-content: center;
        }
        .myTabs{
            margin:25px 10px;
            max-width:100%;
            width: 45%;
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
