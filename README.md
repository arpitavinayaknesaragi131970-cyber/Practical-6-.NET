# Practical-6-.NETProductsController.cs
    using Practical_6demo.Models;

    using System;
    using System.Collections.Generic;
    using System.Linq;
    using System.Web;
    using System.Web.Mvc;

    namespace Practical_6demo.Controllers
    {  
   
    public class ProductsController : Controller
    {
        
        // GET: Products
        
        public ActionResult Index()
        {
            
            List<Products> products = new List<Products>();
           
            Products p1 = new Products();
            p1.Id = 1;
            p1.Name ="Laptop";
            p1.Category = "Electronics";
            p1.Price = 75000;
            p1.Description = "HP Laptop";
            
            Products p2 = new Products();
            p2.Id = 2;
            p2.Name = "Mobile";
            p2.Category = "Electronics";
            p2.Price = 90000;
            p2.Description = "Iphone";
            Products p3 = new Products();
            p3.Id = 3;
            p3.Name = "Car";
            p3.Category = "Automobile";
            p3.Price = 3000000;
            p3.Description = "Hyundai";
            Products p4 = new Products();
            p4.Id = 4;
            p4.Name = "Refrigerator";
            p4.Category = "Home Appliance";
            p4.Price = 45000;
            p4.Description = "LG Refrigerator";
            Products p5 = new Products();
            p5.Id = 5;
            p5.Name = "Bicycle";
            p5.Category = "Sports";
            p5.Price = 18000;
            p5.Description = "Mountain Bike";
            products.Add(p1);
            products.Add(p2);
            products.Add(p3);
            products.Add(p4);
            products.Add(p5);
            return View(products);
        }
    }
    }

    Products.cs

    using System;
    using System.Collections.Generic;
    using System.Linq;
    using System.Web;

    namespace Practical_6demo.Models
    {
    public class Products
    {
        public int Id { get; set; }
        public string Name { get; set; }
        public string Category { get; set; }
        public decimal Price { get; set; }
        public string Description { get; set; }
    }
    }

    Index.cshtml

    @model List<Practical_6demo.Models.Products>

    <h2>Product Catalog</h2>
     <table border="1" cellpadding="8">
    <tr>
        <th>Id</th>
        <th>Name</th>
        <th>Category</th>
        <th>Price</th>
        <th>Description</th>
    </tr>

    @foreach (var product in Model)
       {
    <tr>
     <td>@product.Id</td>
     <td>@product.Name</td>
     <td>@product.Category</td>
     <td>₹ @product.Price</td>
     <td>@product.Description</td>
    </tr>}
    </table>























