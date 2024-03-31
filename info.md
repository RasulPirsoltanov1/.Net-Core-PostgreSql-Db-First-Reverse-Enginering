Please Copy-Paste Following Commands in Tools=>Nuget Package Manager==>Nuget Package Manger Console
`` 
Install-Package Microsoft.VisualStudio.Web.CodeGeneration.Design
Install-Package Microsoft.EntityFrameworkCore
Install-Package Microsoft.EntityFrameworkCore.Tools
Install-Package Microsoft.EntityFrameworkCore.Design
Install-Package Microsoft.EntityFrameworkCore.Relational
Install-Package Microsoft.EntityFrameworkCore.Relational.Design
Install-Package Npgsql
Install-Package Npgsql.EntityFrameworkCore.PostgreSQL
Install-Package npgsql.EntityFrameworkCore.PostgreSQL.Design
For the Last Command you Need to Press Enter Button on keyboad. Please note, I haven't placed any version numbers.
After all packages are installed, Copy-Paste Following Code in the Same Nuget Manager Console
 Scaffold-DbContext “Server=localhost;Database=YourDataBaseName;Username=YourPostgreSQLDatabseUserName;Password=YourPassword;Persist Security Info=True” Npgsql.EntityFrameworkCore.PostgreSQL -OutputDir Models

Please Note that the Last Term Models is the Folder Name where the Context Files will be Saved. If the Output Directory/Folder Name doesn't Exist, then the Build Failed error will appear

I am sure it will work Because it worked for me.
