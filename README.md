# DeploymentData

Angular Deployment Process :

1.Install IIS first
2.Install Asp.NET core Sdk (check version)
  https://learn.microsoft.com/en-us/aspnet/core/host-and-deploy/aspnet-core-module?view=aspnetcore-8.0

3. hosting bundle 
   https://learn.microsoft.com/en-us/aspnet/core/host-and-deploy/iis/hosting-bundle?view=aspnetcore-7.0
   
4. Ng build that will create dist folder in project.

5. add in app.routing.module file 
   imports: [RouterModule.forRoot(routes,{useHash:true})],
   to add remote path instead of local path.
       
6. Create new folder in C then copy all the files in dist folder and paste in that folder.

7. IIS configuration for creating website:
   i. right click on site go to add website 
   ii. Give any name to site 
   iii. select physical path (newly created folders path)   
   iv. changed the port number.  OK 


Backend Process :

1. Note : before publish   we need to comment this lines , there should not been development envioronment selected 

       e.g.
       // Configure the HTTP request pipeline.
       //if (app.Environment.IsDevelopment())
      //{
         app.UseSwagger();
         app.UseSwaggerUI();
      //} 

      After commenting this build project then published it choose newly created folder's path and publish it.
