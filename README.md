# BootstrapJumbtron
## Learning Objectives
* Using bootstrap with Spring Boot

## The Walkthrough

1. Create a Spring Boot Application
	* Name it Jumbotron
	* Add the dependencies for the web and for thymeleaf
	* Hit next until you finish the wizard, and then wait until it's done.

2. Create a Controller
	* Right click on com.example.demo and click New -> Class
	* Name it HomeController.java
	* Edit it to look like this:
```java
import org.springframework.stereotype.Controller;
import org.springframework.web.bind.annotation.RequestMapping;

@Controller
public class HomeController {

    @RequestMapping("/")
    public String index(){
        return "index";
    }
}
```

3. Create a Template
  * Right click on templates and click New -> Html
	* Name it index.html
	* Edit it to look like this:
```html
<!DOCTYPE html>
<html lang="en" xmlns:th="www.thymeleaf.org">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width,initial-scale=1">
    <title>Bootstrap 101 template</title>
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.3/css/bootstrap.min.css" integrity="sha384-MCw98/SFnGE8fJT3GXwEOngsV7Zt27NXFoaoApmYm81iuXoPkFOJwJ8ERdknLPMO" crossorigin="anonymous">
</head>
<body>
	<div class="container">
	<h2>Jumbotron inside the container class</h2>
	<div class="jumbotron">
			<h1>Hello world!</h1>
			<p>...</p>
			<p><a href="#" class="btn btn-primary btn-lg" role="button">Learn
			more</a></p>
	</div>
</div>

<h2>Jumbotron outside the container class</h2>
<div class="jumbotron">
	<h1>Hello world!</h1>
	<p>...</p>
	<p><a href="#" class="btn btn-primary btn-lg" role="button">Learn
			more</a></p>
</div>
<script src="https://ajax.googleapis.com/ajax/libs/jquery/1.12.4/jquery.min.js"></script>
</body>
</html>
```


4. Run your application and open a browser, if you type in the URL http://localhost:8080 you should see this:
![](https://github.com/ajhenley/unofficialguides/blob/master/IntroToSpringBoot/img/Lesson11.png)


## What is Going On

Congratulations! You have created your first styled HTML page. This is a page that includes the Bootstrap libary, which is a number of CSS and JavaScript files that you can use to style your pages. To find out more about how to style your pages, go to the [Twitter Boostsrap website](http://getbootstrap.com/components).

### The Controller
Here, the default route maps to index.html.


### The View
Jumbotron is a style content of Bootstrap that is used to highlight the important section of the page. It is usually placed at the top of a website.
It is displayed with gray box with rounded corners and the text inside the box is enlarged.
If jumbotron placed outside of the container class, then the it will go to the full width of the browser. 

