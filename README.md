. npm create vite@latest
. npm install react-icons
. npm install react-router-dom 
. npm install axios 


Create a dynamic page with the help of react-router-dom 

import {createBrowserRouter , RouterProvider} form "react-router-dom";

import { Home } form "./pages/Home";

const router = createBrowserRouter([
    {
        path : "/",
        element:<Home / >,
    },
    {

    }
]) 

const App = () => {
    return <RouterProvider  router={router}></RouterProvider>;
}; 



... Main ... 
create a new folder insite src name components and  UI after that in components their is Layout folder also and in the layout folder create AppLayout.jsx file... And in the UI folder create two file name Headers.jsx and another one that is Footers.jsx.... 


to print the content of the other file. Then we can use the <Outlet> .... 


//// Form error Page the react already gave the pre-Built functiuonality in the react.... errorElement:<ErrorPage />  /// Also create the ErrorPage.jsx insite the UI folder... 


/// About section ///
in the about section. we used to fetch the api data with the help of react 
in this first we import the  

import countryFacts from "../api/countryData.json";

to fetch the multiple data with the help of api we used map method 
countryFacts.map((country) => {
    return(
        <div className="card" key={}>
    )
})



////// Whenever we create by default formData.entries is created to show the data in it ///// 



/////// to submit the form you should only write //// 
const handleFormSubmit = (formData) => {
        const formInputData = Object.fromEntries(formData.entries());
    };  


//// if we access the icon in the json file then first we create a object them after that we can access the icon in the json file //// 
//// and also it is required to import the library to acces the element from the json to the footer.jsx file and in this we call the value of the json file.... 


/// know work with the country page /// 


/// we fetch the real world api with the help of react /// 
import axios from "axios";

axios.create({
    baseURL: "https://restcountries.com/v3.1/all?fields=name,population,region,capital,flags",
});  


///// in axios it is very easy to fetch the data from the api /// there is no required to async of the element //// 

const [isPending, startTransition] = useTransition();
const [countries , setCountries] = useState([]);

useEffect(() => { 
    startTransition(async() => {
        const res = await getCountryData();
        setCountries(res.data);
    })
},[]);#   W o r l d _ A t l a s  
 