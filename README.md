Made Simple Symfony 3 starter kit
=======

###Documentation under construction###

<div class="col-md-12 ">
                <div class="row block-row">
                    <div class="col-md-12 homeText">
                        <p>Hi! i share my symfony 3 starter kit. It's certainly not perfect, feel free to use and improve. It comes with a bunch of nice bundle and a couple of developpement made by me, for image management with&nbsp;&nbsp;drag and drop and multi upload, simple comment system, simple widgets (very simple). It's realy not a cms, you're not supposed to take everything like it is but modify it for your purpose. With this starter, you&nbsp;can manage : Users,&nbsp;Pages, Articles, Imagess, Comments, Settings</p>
                    </div>

                    <div class="col-md-6 block">
                        <h1><i class="fa fa-cog"></i>&nbsp;Main Entity Management</h1>

                        <p>Easy User management with  <a href="http://symfony.com/doc/current/bundles/FOSUserBundle/index.html" style="line-height: 1.6;">FosUserBundle</a></p>

                        <p>Easy Backoffice with the excellent <a href="https://github.com/javiereguiluz/EasyAdminBundle" style="line-height: 1.6;">EasyAdminBundle</a>, config file is config/easy_admin.yml</p>

                        <p>Esay Uploading with <a href="https://github.com/dustin10/VichUploaderBundle">VichUploaderBundle</a>, config file is config/vich_uploader.yml, variable path are in config/parameters.yml</p>

                        <p>Easy Image format gestion with&nbsp;<a href="https://github.com/liip/LiipImagineBundle">ImagineBundle</a></p>

                        <p>Easy text editing with <a href="https://github.com/egeloen/IvoryCKEditorBundle">IvoryCKEditorBundle</a></p>
                    </div>

                    <div class="col-md-6">
                        <h1><i class="fa fa-arrow-down"></i>&nbsp; Inside</h1>

                        <ul style="padding-left: 0;">
                            <li>Symfony\Bundle\FrameworkBundle\FrameworkBundle</li>
                            <li>Symfony\Bundle\SecurityBundle\SecurityBundle</li>
                            <li>Symfony\Bundle\TwigBundle\TwigBundle</li>
                            <li>Symfony\Bundle\MonologBundle\MonologBundle</li>
                            <li>Symfony\Bundle\SwiftmailerBundle\SwiftmailerBundle</li>
                            <li>Symfony\Bundle\AsseticBundle\AsseticBundle</li>
                            <li>Doctrine\Bundle\DoctrineBundle\DoctrineBundle</li>
                            <li>Sensio\Bundle\FrameworkExtraBundle\SensioFrameworkExtraBundle</li>
                            <li>FOS\UserBundle\FOSUserBundle</li>
                            <li>FOS\JsRoutingBundle\FOSJsRoutingBundle</li>
                            <li>JavierEguiluz\Bundle\EasyAdminBundle\EasyAdminBundle</li>
                            <li>Vich\UploaderBundle\VichUploaderBundle</li>
                            <li>Liip\ImagineBundle\LiipImagineBundle</li>
                            <li>Ivory\CKEditorBundle\IvoryCKEditorBundle</li>
                        </ul>
                    </div>
                </div>
<div class="row block-row">
                    <div class="col-md-6">
                        <h1><i class="fa fa-image"></i>&nbsp; Image Made Simple <br><small>MultiUpload, Drag and drop, sortable, resize</small></h1>
                        <p>
                            Juste use Imageable Trait in your entity

</p><pre>use AppBundle\Traits\Imageable;

class Page
{
    use Imageable;

}

</pre>
                        That's it! After that you can retreive your image with <code>entity.getImages()</code><br><br>
                        To show them on your view : <code>asset("uploads/image/"~image.image)|imagine_filter('thumbnail')</code><br><br>
                        Filters are defined in <code>app/config/liip_imagine.yml</code>
                        <p></p>

                    </div>
                    <div class="col-md-6">
                        <h1><i class="fa fa-map"></i>&nbsp; Map Made Simple<br><small>Just a tiny widget</small></h1>
                        <p>
                            Just do <code>app_twig.getMap(your_lat,your_lng)|raw </code> on your view
                        </p>
                        <p>
                            You can change it easy on <code>app/Resources/views/component/map</code>
                        </p>


                    </div>
                </div>
                <br><br>
                <div class="row block-row">
                    <div class="col-md-6">
                        <h1><i class="fa fa-comment"></i>&nbsp; Comment Made Simple</h1>
                        <p>
                            Juste use Imageable Trait in your entity
</p><pre>
use AppBundle\Traits\Commentable;

class Page
{
    use Commentable;

}

</pre>
                        <p>That's it! After that you can retreive your comment with <code>entity.getComments()</code>  </p>
                        <p>To get the form : <code>app_twig.getCommentForm(entity)|raw</code>  </p>
                        <p>You can allow and disallow anonymous comments by changing parameter allow_anonymous_comments to 0 or nop or non or no   </p>
                        <p>You can set comments at validated state by default or not by changing parameter validated_comments_by_defaut to 0 or nop or non or no   </p>

                    </div>

                </div>
                <div class="row block-row">
                    <div class="col-md-6">
                        <h1><i class="fa fa-area-chart"></i>&nbsp;Tracking Made Simple<br><small>Just a tiny widget again</small></h1>
                        <p>
                            Just do <code>app_twig.getAnalitycsTracking('your tracking code')|raw </code> on your view
                        </p>
                        <p>
                            If you create a parameter named tracking_code just do  <code>app_twig.getAnalitycsTracking()|raw </code>
                        </p>
                        <p>
                            It will out put the defualt analitycs code tracking
                        </p>
<pre>    var _gaq = _gaq || [];
    _gaq.push(['_setAccount', 'your_code' ]);
    _gaq.push(['_trackPageview']);

    (function() {
        var ga = document.createElement('script'); ga.type = 'text/javascript'; ga.async = true;
        ga.src = ('https:' == document.location.protocol ? 'https://ssl' : 'http://www') + '.google-analytics.com/ga.js';
        var s = document.getElementsByTagName('script')[0]; s.parentNode.insertBefore(ga, s);
    })();
</pre>
                        <p>
                            Feel free to customize it, it's located in <code>views/component/analitycs/</code>
                        </p>
                    </div>
                    <div class="col-md-6">
                        <h1><i class="fa fa-file-image-o"></i>&nbsp;Slider Made Simple<br><small>Just a tiny widget again ( yeah i know.. )</small></h1>
                        <p>
                            Just do <code>app_twig.getSlider(entity)|raw </code> on your view
                        </p>
                        <p>
                            It's the bootstrap slider, for now, it's made for imgeable entities, feel free to make your own :)
                        </p>
                        <div>
                            <div id="slider" class="carousel slide" data-ride="carousel">
    <!-- Indicators -->
    <ol class="carousel-indicators">
                <li data-target="#slider" data-slide-to="1" class=""></li>
                <li data-target="#slider" data-slide-to="2" class="active"></li>
                <li data-target="#slider" data-slide-to="3" class=""></li>
                <li data-target="#slider" data-slide-to="4" class=""></li>
                <li data-target="#slider" data-slide-to="5" class=""></li>
                <li data-target="#slider" data-slide-to="6" class=""></li>
                <li data-target="#slider" data-slide-to="7" class=""></li>
                <li data-target="#slider" data-slide-to="8" class=""></li>
            </ol>

                        </div>
                        <p>
                           It's located in <code>views/component/slider/</code>
                        </p>
                    </div>
                </div>


                <div class="row block-row">
                    <div class="col-md-6">
                        <h1><i class="fa fa-envelope"></i>&nbsp;Contact Made Simple</h1>
                        <div class="panel panel-default">
    <h3>Contact me</h3>
    <div class="alert hide" id="contact-return">

    </div>
    <form name="contact" method="post" action="/app_dev.php/contact/send"><div id="contact-form"><div class="form-group is-empty"><input type="text" id="contact_name" name="contact[name]" required="required" placeholder="Name" class="form-control"></div><div class="form-group is-empty"><input type="email" id="contact_email" name="contact[email]" required="required" placeholder="Email" class="form-control"></div><div class="form-group is-empty"><input type="text" id="contact_subject" name="contact[subject]" required="required" placeholder="Subject" class="form-control"></div><div class="form-group is-empty"><textarea id="contact_text" name="contact[text]" required="required" placeholder="Message" class="form-control"></textarea></div><div class="form-group"><button type="submit" id="contact_Send" name="contact[Send]" class="btn btn-primary btn">Send</button></div></div></form>
</div>

                    </div>
                    <div class="col-md-6">
                        <div class="col-md-12">
                            <h1><i class="fa fa-cogs "></i>&nbsp;Settings</h1>
                            <p>Some settings are locked, but you can remove them by editing the file <code>AppBundl/Listener/LifeCycleSliner.php</code></p>
                            <p>List of default settings : </p>
                            <ul style="padding : 0">
                                <li>    - Default Slug route	</li>
                                <li>	- Analitycs tracking  </li>
                                <li>    - By default, comments published without moderation</li>
                                <li>	- Allow anonymous comment</li>
                                <li>	- Contact Email	</li>
                                <li>	- Website description </li>
                                <li>	- Website name</li>
                            </ul>
                        </div>
                        <div class="col-md-12">
                            <h1><i class="fa fa-wrench"></i>&nbsp;Installation Made Simple</h1>
                            <p><code>Git clone blablabla</code></p>
                            <p><code>composer install</code></p>
                            <p><code>php bin/console app:init</code></p>
                            <p>Answer all question</p>
                            <p>Start to work :)</p>
                        </div>

                    </div>


                </div>


                <div class="row block-row">
                    <div class="col-md-6">
                        <h1><i class="fa fa-user"></i>&nbsp;Who am I ?</h1>
                        <p>Hey ! I'm Sohrab</p>
                        <p>I'm fullstack web developper freelance based in Lyon, feel free to contact me with the form above</p>
                    </div>
                </div>


            </div>