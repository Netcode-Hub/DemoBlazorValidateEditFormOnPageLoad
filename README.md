# Introducing My Blazor Nugget Package🌠: Simplify EditForm Validation on Page Initialization in .NET 8 Blazor🔥

# How to Use The Package
# Install the package
    NetcodeHub.Packages.Components.OnPageLoadValidation
    
# Start Using in Editform to Enforce its Validation on Page Startup
    <h1>Default Blazor Components</h1>
    <EditForm Model="ProductModel" OnValidSubmit="SaveProduct">
        <DataAnnotationsValidator />
        <ValidationSummary/>
        <NetcodeHub.Packages.Components.OnPageLoadValidation.NetcodeHubEditFormValidatorOnPageLoad />
        <div class="mt-3">
            <label class="form-label">Name</label>
            <InputText @bind-Value="ProductModel.Name" class="form-control" />
            <ValidationMessage For="() => ProductModel.Name" />
        </div>
        <div class="mt-3">
            <label class="form-label">Quantity</label>
            <InputNumber @bind-Value="ProductModel.Quantity" class="form-control" />
            <ValidationMessage For="() => ProductModel.Quantity" />
        </div>
        <div class="mt-3">
            <label class="form-label">Description</label>
            <InputTextArea @bind-Value="ProductModel.Description" class="form-control" />
            <ValidationMessage For="() => ProductModel.Description" />
        </div>
    
        <button type="submit" class="btn btn-primary mt-3 mb-5">Save</button>
    </EditForm>

    @code {
        Product ProductModel = new();
    
        void SaveProduct()
        {
    
        }
    
        public class Product
        {
            public int Id { get; set; }
            [Required, MinLength(5), MaxLength(10)]
            public string? Name { get; set; }
            [Required, Range(1, 10)]
            public int Quantity { get; set; }
            [Required, MinLength(5), MaxLength(10)]
            public string? Description { get; set; }
        }
    }
![image](https://github.com/Netcode-Hub/DemoBlazorValidateEditFormOnPageLoad/assets/110794348/ff7aca1d-2fcf-4b96-a052-171ab1e01c62)
![image](https://github.com/Netcode-Hub/DemoBlazorValidateEditFormOnPageLoad/assets/110794348/6ef3a9a9-cddb-4bb1-acbc-192a67d52e8b)
![image](https://github.com/Netcode-Hub/DemoBlazorValidateEditFormOnPageLoad/assets/110794348/8e42ac42-3583-4547-9430-5c9450d661a4)

# When the page starts, Validation begins
![image](https://github.com/Netcode-Hub/NetcodeHub.Packages.Components.OnPageLoadValidation/assets/110794348/6e37a69d-f054-4dca-8c8c-2a9adbdc99a3)

# Here's a follow-up section to encourage engagement and support for Netcode-Hub:
🌟 Get in touch with Netcode-Hub! 📫
1. GitHub: [Explore Repositories](https://github.com/Netcode-Hub/Netcode-Hub) 🌐
2. Twitter: [Stay Updated](https://twitter.com/NetcodeHub) 🐦
3. Facebook: [Connect Here](https://web.facebook.com/NetcodeHub) 📘
4. LinkedIn: [Professional Network](https://www.linkedin.com/in/netcode-hub-90b188258/) 🔗
5. Email: Email: [business.netcodehub@gmail.com](mailto:business.netcodehub@gmail.com) 📧
