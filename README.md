# Description
Piece of code which help to customize Wordpress Logon page

# HowTo

Insert bellow code and edit values with your params into function.php file

```
// Change admin login logo
function my_login_logo() { ?>
<style type="text/css">
#login h1 a, .login h1 a {
background-image: url(<?php echo get_stylesheet_directory_uri(); ?>/images/logo.jpg);
height:72px;
width:300px;
background-size: 300px 72px;
background-repeat: no-repeat;
padding-bottom: 30px;
}
</style>
<?php }
add_action( 'login_enqueue_scripts', 'my_login_logo' );
 
// Change admin login logo link
function my_login_logo_url() {
return home_url();
}
add_filter( 'login_headerurl', 'my_login_logo_url' );
 
// Change Title description
function my_login_logo_url_title() {
return 'Title description on hover';
}
add_filter( 'login_headertitle', 'my_login_logo_url_title' );
```
