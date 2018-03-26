# Converter Projeto Portable Class Library para .NET Standard

Não há razão para não usar o .NET Standard 2.0 neste ponto. 
Ele suporta todas as suas plataformas, incluindo todas as plataformas Xamarin.
Além disso, o .NET Standard é o futuro! Ele substitui o PCL e o Shared Projects.

É muito simples

- Descarregue seu projeto PCL (clique com o botão direito -> descarregar) 
e comece a editá-lo (direito -> clique em editar)
Exclua tudo no csproj e insira isto:

```
<Project Sdk = "Microsoft.NET.Sdk">
  <PropertyGroup>
    <TargetFramework> netstandard2.0 </ TargetFramework>
  </ PropertyGroup>

  <ItemGroup>
    <! - <PackageReference Include = "" Versão = "" /> ->
  </ ItemGroup>

</ Project>

```

- Adicione novamente NuGets, simplesmente abra o arquivo packages.config e adicione as referências do pacote acima, 
ou através do gerenciador de pacotes NuGet.

```
<Project Sdk="Microsoft.NET.Sdk">

  <PropertyGroup>
    <TargetFramework>netstandard2.0</TargetFramework>
  </PropertyGroup>

  <ItemGroup>
    <PackageReference Include="Newtonsoft.Json" Version="10.0.3" />
    <PackageReference Include="Xamarin.Forms" Version="2.5.0.122203" />
  </ItemGroup>

</Project>
```

- Exclua AssemblyInfo.cs (isso agora está no csproj) e 
packages.config (também no csproj via PackageReference)

Pronto você terminou! 
Bem-vindo ao mundo do .NET Standard 2.0! 

Mais Exemplos:

James Montemagno
https://montemagno.com/how-to-convert-a-pcl-library-to-net-standard-and-keep-git-history/

Xamarin Help
https://xamarinhelp.com/upgrade-pcl-net-standard-class-library/
