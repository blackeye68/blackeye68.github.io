<!-- ---
layout: post
title:  "Top 50 câu hỏi phỏng vấn về ASP.NET MVC cùng câu trả lời"
author: john
categories: [ interview, questions, dotnet_mvc ]
image: assets/images/6.jpg
--- -->

### 1. WHAT IS ASP.NET MVC?

ASP.NET MVC is a web application Framework. It is light weight and highly testable Framework. MVC separates application into three components - **Model**, **View** and **Controller**.

### 2. CAN YOU EXPLAIN MODEL, CONTROLLER AND VIEW IN MVC?

* **Model** — It’s a business entity and it is used to represent the application data.

* **Controller** — Request sent by the user always scatters through controller and it’s responsibility is to redirect to the specific view using View() method.

* **View** — It’s the presentation layer of MVC.

### 3. EXPLAIN THE NEW FEATURES ADDED IN VERSION 4 OF MVC (MVC4)?

Following are features added newly –

→Asynchronous controller task support.

→Bundling the java scripts.

→Segregating the configs for MVC routing, Web API, Bundle etc.

→Mobile templates

→Added ASP.NET Web API template for creating REST based services.

→Asynchronous controller task support.

→Bundling the java scripts.

→Segregating the configs for MVC routing, Web API, Bundle etc.

### 4. CAN YOU EXPLAIN THE PAGE LIFE CYCLY OF MVC?

Below are the processed followed in the sequence -

-> App initialization (khởi tạo ứng dụng)

-> Routing

-> Instantiate and execute controller

-> 5) What are the advantages of MVC over ASP.NET?

→Provides a clean separation of concerns among UI (Presentation layer), model (Transfer objects/Domain Objects/Entities) and Business Logic (Controller).

→Easy to UNIT Test.

→Improved reusability of model and views. We can have multiple views which can point to the same model and vice versa.

→Improved structuring of the code.

6) What is Separation of Concerns in ASP.NET MVC?

It’s is the process of breaking the program into various distinct features which overlaps in functionality as little as possible. MVC pattern concerns on separating the content from presentation and data-processing from content.

7) What is Razor View Engine?

Razor is the first major update to render HTML in MVC 3. Razor was designed specifically for view engine syntax. Main focus of this would be to simplify and code-focused templating for HTML generation. Below is the sample of using Razor:

@model MvcMusicStore.Models.Customer
@{ViewBag.Title = “Get Customers”;}
<div class=”cust”> <h3><em>@Model.CustomerName</em> </h3>
8) What is the meaning of Unobtrusive JavaScript?

This is a general term that conveys a general philosophy, similar to the term REST (Representational State Transfer). Unobtrusive JavaScript doesn’t intermix JavaScript code in your page markup.

Eg : Instead of using events like onclick and onsubmit, the unobtrusive JavaScript attaches to elements by their ID or class based on the HTML5 data- attributes.

9) What is the use of ViewModel in MVC?

ViewModel is a plain class with properties, which is used to bind it to strongly typed view. ViewModel can have the validation rules defined for its properties using data annotations.

10) What you mean by Routing in MVC?

Routing is a pattern matching mechanism of incoming requests to the URL patterns which are registered in route table. Class — “UrlRoutingModule” is used for the same process.

11) What are Actions in MVC?

Actions are the methods in Controller class which is responsible for returning the view or json data. Action will mainly have return type — “ActionResult” and it will be invoked from method — “InvokeAction()” called by controller.

12) What is Attribute Routing in MVC?

ASP.NET Web API supports this type routing. This is introduced in MVC5. In this type of routing, attributes are being used to define the routes. This type of routing gives more control over classic URI Routing. Attribute Routing can be defined at controller level or at Action level like –

[Route(“{action = TestCategoryList}”)] — Controller Level
[Route(“customers/{TestCategoryId:int:min(10)}”)] — Action Level
13) How to enable Attribute Routing?

Just add the method — “MapMvcAttributeRoutes()” to enable attribute routing as shown below

public static void RegistearRoutes(RouteCollection routes)

{

routes.IgnoareRoute(“{resource}.axd/{*pathInfo}”);

//enabling attribute routing

routes.MapMvcAttributeRoutes();

//convention-based routing

routes.MapRoute

(

name: “Default”,

url: “{controller}/{action}/{id}”,

defaults: new { controller = “Customer”, action = “GetCustomerList”, id = UrlParameter.Optional }

);

}

14) Explain JSON Binding?

JavaScript Object Notation (JSON) binding support started from MVC3 onwards via the new JsonValueProviderFactory, which allows the action methods to accept and model-bind data in JSON format. This is useful in Ajax scenarios like client templates and data binding that need to post data back to the server.

15) Explain Dependency Resolution?

Dependency Resolver again has been introduced in MVC3 and it is greatly simplified the use of dependency injection in your applications. This turn to be easier and useful for decoupling the application components and making them easier to test and more configurable.

16) Explain Bundle.Config in MVC4?

“BundleConfig.cs” in MVC4 is used to register the bundles by the bundling and minification system. Many bundles are added by default including jQuery libraries like — jquery.validate, Modernizr, and default CSS references.

17) How route table has been created in ASP.NET MVC?

Method — “RegisterRoutes()” is used for registering the routes which will be added in “Application_Start()” method of global.asax file, which is fired when the application is loaded or started.

18) Which are the important namespaces used in MVC?

Below are the important namespaces used in MVC -

System.Web.Mvc

System.Web.Mvc.Ajax

System.Web.Mvc.Html

System.Web.Mvc.Async

19) What is ViewData?

Viewdata contains the key, value pairs as dictionary and this is derived from class — “ViewDataDictionary“. In action method we are setting the value for viewdata and in view the value will be fetched by typecasting.

20) What is the difference between ViewBag and ViewData in MVC?

ViewBag is a wrapper around ViewData, which allows to create dynamic properties. Advantage of viewbag over viewdata will be –

In ViewBag no need to typecast the objects as in ViewData.

ViewBag will take advantage of dynamic keyword which is introduced in version 4.0. But before using ViewBag we have to keep in mind that ViewBag is slower than ViewData.

21) Explain TempData in MVC?

TempData is again a key, value pair as ViewData. This is derived from “TempDataDictionary” class. TempData is used when the data is to be used in two consecutive requests, this could be between the actions or between the controllers. This requires typecasting in view.

22) What are HTML Helpers in MVC?

HTML Helpers are like controls in traditional web forms. But HTML helpers are more lightweight compared to web controls as it does not hold viewstate and events.

HTML Helpers returns the HTML string which can be directly rendered to HTML page. Custom HTML Helpers also can be created by overriding “HtmlHelper” class.

23) What are AJAX Helpers in MVC?

AJAX Helpers are used to create AJAX enabled elements like as Ajax enabled forms and links which performs the request asynchronously and these are extension methods of AJAXHelper class which exists in namespace — System.Web.Mvc.

24) What are the options can be configured in AJAX helpers?

Below are the options in AJAX helpers –

Url — This is the request URL.

Confirm — This is used to specify the message which is to be displayed in confirm box.

OnBegin — Javascript method name to be given here and this will be called before the AJAX request.

OnComplete — Javascript method name to be given here and this will be called at the end of AJAX request.

OnSuccess — Javascript method name to be given here and this will be called when AJAX request is successful.

OnFailure — Javascript method name to be given here and this will be called when AJAX request is failed.

UpdateTargetId — Target element which is populated from the action returning HTML.

25) What is Layout in MVC?

Layout pages are similar to master pages in traditional web forms. This is used to set the common look across multiple pages. In each child page we can find — /p>

@{

Layout = “~/Views/Shared/TestLayout1.cshtml”;

}

This indicates child page uses TestLayout page as it’s master page.

26) Explain Sections is MVC?

Section are the part of HTML which is to be rendered in layout page. In Layout page we will use the below syntax for rendering the HTML –

@RenderSection(“TestSection”)

And in child pages we are defining these sections as shown below –

@section TestSection{

<h1>Test Content</h1>

}

If any child page does not have this section defined then error will be thrown so to avoid that we can render the HTML like this –

@RenderSection(“TestSection”, required: false)

27) Can you explain RenderBody and RenderPage in MVC?

RenderBody is like ContentPlaceHolder in web forms. This will exist in layout page and it will render the child pages/views. Layout page will have only one RenderBody() method. RenderPage also exists in Layout page and multiple RenderPage() can be there in Layout page.

28) What is ViewStart Page in MVC?

This page is used to make sure common layout page will be used for multiple views. Code written in this file will be executed first when application is being loaded.

29) Explain the methods used to render the views in MVC?

Below are the methods used to render the views from action -

View() — To return the view from action.

PartialView() — To return the partial view from action.

RedirectToAction() — To Redirect to different action which can be in same controller or in different controller.

Redirect() — Similar to “Response.Redirect()” in webforms, used to redirect to specified URL.

RedirectToRoute() — Redirect to action from the specified URL but URL in the route table has been matched.

30) What are the sub types of ActionResult?

ActionResult is used to represent the action method result. Below are the subtypes of ActionResult –

ViewResult

PartialViewResult

RedirectToRouteResult

RedirectResult

JavascriptResult

JSONResult

FileResult

HTTPStatusCodeResult

31) What are Non Action methods in MVC?

In MVC all public methods have been treated as Actions. So if you are creating a method and if you do not want to use it as an action method then the method has to be decorated with “NonAction” attribute as shown below –

[NonAction]

public void TestMethod()

{

// Method logic

}

32) How to change the action name in MVC?

“ActionName” attribute can be used for changing the action name. Below is the sample code snippet to demonstrate more –

[ActionName(“TestActionNew”)]

public ActionResult TestAction()

{

return View();

}

So in the above code snippet “TestAction” is the original action name and in “ActionName” attribute, name — “TestActionNew” is given. So the caller of this action method will use the name “TestActionNew” to call this action.

33) What are Code Blocks in Views?

Unlike code expressions that are evaluated and sent to the response, it is the blocks of code that are executed. This is useful for declaring variables which we may be required to be used later.

@{

int x = 123;

string y = “aa”;

}

34) What is the “HelperPage.IsAjax” Property?

The HelperPage.IsAjax property gets a value that indicates whether Ajax is being used during the request of the Web page.

35) How we can call a JavaScript function on the change of a Dropdown List in MVC?

Create a JavaScript method:

<script type=”text/javascript”>

function DrpIndexChanged() { }

</script>

Invoke the method:

<%:Html.DropDownListFor(x => x.SelectedProduct, new SelectList(Model.Customers, “Value”, “Text”), “Please Select a Customer”, new { id = “ddlCustomers”, onchange=” DrpIndexChanged ()” })%>

36) What are Validation Annotations?

Data annotations are attributes which can be found in the “System.ComponentModel.DataAnnotations” namespace. These attributes will be used for server-side validation and client-side validation is also supported. Four attributes — Required, String Length, Regular Expression and Range are used to cover the common validation scenarios.

37) Why to use Html.Partial in MVC?

This method is used to render the specified partial view as an HTML string. This method does not depend on any action methods. We can use this like below –

@Html.Partial(“TestPartialView”)

38) What is Html.RenderPartial?

Result of the method — “RenderPartial” is directly written to the HTML response. This method does not return anything (void). This method also does not depend on action methods. RenderPartial() method calls “Write()” internally and we have to make sure that “RenderPartial” method is enclosed in the bracket. Below is the sample code snippet –@{Html.RenderPartial(“TestPartialView”); }

39) What is RouteConfig.cs in MVC 4?

“RouteConfig.cs” holds the routing configuration for MVC. RouteConfig will be initialized on Application_Start event registered in Global.asax.

40) What are Scaffold templates in MVC?

Scaffolding in ASP.NET MVC is used to generate the Controllers,Model and Views for create, read, update, and delete (CRUD) functionality in an application. The scaffolding will be knowing the naming conventions used for models and controllers and views.

41) Explain the types of Scaffoldings.

Below are the types of scaffoldings –

Empty

Create

Delete

Details

Edit

List

42) Can a view be shared across multiple controllers? If Yes, How we can do that?

Yes, we can share a view across multiple controllers. We can put the view in the “Shared” folder. When we create a new MVC Project we can see the Layout page will be added in the shared folder, which is because it is used by multiple child pages.

43) What are the components required to create a route in MVC?

Name — This is the name of the route.

URL Pattern — Placeholders will be given to match the request URL pattern.

Defaults –When loading the application which controller, action to be loaded along with the parameter.

44) Why to use “{resource}.axd/{*pathInfo}” in routing in MVC?

Using this default route — {resource}.axd/{*pathInfo}, we can prevent the requests for the web resources files like — WebResource.axd or ScriptResource.axd from passing to a controller.

45) Can we add constraints to the route? If yes, explain how we can do it?

Yes we can add constraints to route in following ways –

Using Regular Expressions

Using object which implements interface — IRouteConstraint.

46) What are the possible Razor view extensions?

Below are the two types of extensions razor view can have –

.cshtml — In C# programming language this extension will be used.

.vbhtml — In VB programming language this extension will be used.

### 47. WHAT IS PartialView IN MVC?

PartialView is similar to UserControls in traditional web forms. For re-usability purpose partial views are used. Since it’s been shared with multiple views these are kept in shared folder. Partial Views can be rendered in following ways –

Html.Partial()

Html.RenderPartial()

### 48. HOW WEB CAN ADD THE CSS IN MVC?

Below is the sample code snippet to add css to razor views –

    <link rel=”StyleSheet” href=”/@Href(~Content/Site.css”)” type=”text/css”/>

### 49. CAN I ADD MVC TESTCASES IN VISUAL STUDIO EXPRESS?

No. We cannot add the test cases in Visual Studio Express edition it can be added only in Professional and Ultimate versions of Visual Studio.

### 50. WHAT IS THE USE .GLIMPSE IN MVC?

Glimpse is an open source tool for debugging the routes in MVC. It is the client side debugger. Glimpse has to be turned on by visiting to local url link -

**_http://localhost:portname//glimpse.axd_**

This is a popular and useful tool for debugging which tracks the speed details, url details etc.