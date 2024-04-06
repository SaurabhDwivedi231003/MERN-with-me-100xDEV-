------------- ROUTING ---------------------

                INTERVIEW NOTES

JARGONS : 
 -> Single Page Application.
 -> Client Side bundle : Complete bundle comes back along with index.html file.
 -> Client side routing.

==> useNavigate() Hook is used for Navigation / Routing in React to prevent from reload.
 
==> Lazy Loading  & Suspense :
    -> Some times happen that user only see landing page and not the full website so why to give them a whole bundle at once.
    -> Better is to load the bundle when user click on the link.
    -> Load entire bundle but give page bundle one by one as user keep on clicking on other pages.
    -> Ek baar me code aa jye , jo jo page click kre uska code ind=creamently usse milte jye

  --> Syntax :
     const Landing = React.lazy(()=> import('./components/Landing'));  
      
      Also wrap inside Suspense :  

      <Suspense fallback={<div>Loading...</div>}>
          <Routes>
                  <Route path="/" element={<Landing />} />
                  <Route path="/home" element={<Home/>} />
          </Routes>
      </Suspense>



JUST TO KNOW : for ROUTE.

// <link></link>    : can also be used for routing but it will only works when user clicks.
    
Some extra coded : 
 function App() { 

    // {/* <div>
    //   <button onClick={()=>{ window.location.href="/home" }}>Home</button>
    //   <button onClick={()=>{ window.location.href="/" }}>Landing</button>
    // </div>
    //     This is not the right way to navigate between pages , because it makes pages reload again and again.
    // */}

    // Also : 
    // <link></link>    : can be used but it will only works when user clicks.
    
    // {/* We will navigate using 'useNavigate()' hook , provided by react-router-dom */}
 
  return (