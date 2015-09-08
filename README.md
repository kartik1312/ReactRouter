# ReactRouter
This is for client side Routing in React. We have made the router to ease the routing in SPA with having change in URI's
1.Introduction 
	We all must be aware of the fact of client side  routing. Well we were exploring the routing capabilities in 		react. We got introduced to react-router. As a newbies to react we were exploring react-router but couldn’t 	able to deduce how it is going to be implemented (no disrespect to Ryan Florence and Michael Jackson).So we 			decided to make our own library  for client side routing. 
	This is our first attempt to write any library and we are open to all sort of suggestions .Please  feel free 		to contribute .
2.Project Details
	js
	+-----hashmap.js
	+------Router.js
3. Expectation
Well this router is mainly for two reasons:
	1.On basis of URI changes it renders the components.
	2.We also tried to maintain the session  of the page on page refresh.
	3.Simple to Use

4. How to Use it
	4.1. In your html import these two scripts i.e. hasmap.js and R3.js.
	4.2. In the body write the script tag .For eg.
		<script src="/javascript/dashboard/hashmap.js" ></script>
		<script src="/javascript/dashboard/router.js" type="text/jsx"></script>
	4.3. Container.js file is that file in which we have mentioned the components to render.
	4.4 So, in the script tag in the body inside the React.render part ,mention the paths as well as according to that path which component you want to render.Foe eg.
		<script type="text/jsx">
            React.render(
            <Container landing="#login">
                  <Tab path="" handler={ LoginModule } />
                  <Tab path="#" handler={ LoginModule } />
                  <Tab path="#login" handler={ LoginModule } />
                  <Tab path="#hmenu" handler={ WelcomeModule } />
                  <Tab path="#hmenu#accounttransfer" handler={ AccountTransferModule } />
                  <Tab path="#hmenu#salesadjustment" handler={ SalesAdjustmentModule } />
                  <Tab path="#hmenu#blocktransfer" handler={ BlockTransferModule } />
                  <Tab path="#hmenu#searchanddisplay" handler={ SearchModule } />
            </Container>
            ,document.body);
      </script>

4.5 And then in container.js declare your components .If you have not declare any kind of documents then it will display :

"The Compoenents  is Wrongly Configured  OR not available .Please click the bac Button to get back into the application".
	 
