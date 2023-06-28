---
title: Linky
publishDate: 11-06-2023 00:00:00
img: /assets/api.jpg
img_alt: API Linky
description: |
  Se connecter a une API Linky
tags:
  - .net core 6
  - C#
  - API
  - Enedis
---

# API to manage linky indicator data

## Technolohies used

- .net core 6
- asp.net
- ef core 7.0.5

## Migration default configuration

This API use by default the SQL Server. It's possible and easily editable to change this.
- The only code to change is the following :

`builder.Services.AddDbContext<LinkyContext>((sp, x) =>
    x.UseSqlServer(sp.GetRequiredService<IConfiguration>().GetConnectionString("DefaultConnection")));`
- And download the adapted library in the Linky.API project, i.e : Microsoft.EntityFrameworkCore.SqlServer

## Deployment

This solution use migartions, to run it you have to use entity framework core commands.
Execute the following commands into package manager console (take care of the default project used, it have to be Linky.API) : `Update-Database`

---

## Conclusion

Ce projet d'API de gestion des données de l'indicateur Linky est développé en utilisant les technologies .NET Core 6, ASP.NET et EF Core 7.0.5. Il offre la possibilité de gérer les informations liées aux compteurs Linky, y compris les relevés de consommation et d'autres indicateurs pertinents.
