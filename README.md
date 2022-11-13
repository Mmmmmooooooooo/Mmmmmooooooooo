<?xml version="1.0" encoding="utf-8"?>
<Project ToolsVersion="15.0" xmlns="http://schemas.microsoft.com/developer/msbuild/2003">
  <Import Project="$(MSBuildExtensionsPath)\$(MSBuildToolsVersion)\Microsoft.Common.props" Condition="Exists('$(MSBuildExtensionsPath)\$(MSBuildToolsVersion)\Microsoft.Common.props')" />
  <PropertyGroup>
    <Configuration Condition=" '$(Configuration)' == '' ">Debug</Configuration>
    <Platform Condition=" '$(Platform)' == '' ">AnyCPU</Platform>
    <ProjectGuid>{EBC8607E-B6BA-4ED6-8848-C78964190641}</ProjectGuid>
    <OutputType>Library</OutputType>
    <AppDesignerFolder>Properties</AppDesignerFolder>
    <RootNamespace>Baby_Mode</RootNamespace>
    <AssemblyName>Baby Mode</AssemblyName>
    <TargetFrameworkVersion>v4.7.2</TargetFrameworkVersion>
    <FileAlignment>512</FileAlignment>
    <Deterministic>true</Deterministic>
  </PropertyGroup>
  <PropertyGroup Condition=" '$(Configuration)|$(Platform)' == 'Debug|AnyCPU' ">
    <DebugSymbols>true</DebugSymbols>
    <DebugType>full</DebugType>
    <Optimize>false</Optimize>
    <OutputPath>bin\Debug\</OutputPath>
    <DefineConstants>DEBUG;TRACE</DefineConstants>
    <ErrorReport>prompt</ErrorReport>
    <WarningLevel>4</WarningLevel>
  </PropertyGroup>
  <PropertyGroup Condition=" '$(Configuration)|$(Platform)' == 'Release|AnyCPU' ">
    <DebugType>pdbonly</DebugType>
    <Optimize>true</Optimize>
    <OutputPath>bin\Release\</OutputPath>
    <DefineConstants>TRACE</DefineConstants>
    <ErrorReport>prompt</ErrorReport>
    <WarningLevel>4</WarningLevel>
  </PropertyGroup>
  <ItemGroup>
    <Reference Include="Assembly-CSharp">
      <HintPath>F:\Program Files (x86)\Steam\steamapps\common\BloonsTD6\MelonLoader\Managed\Assembly-CSharp.dll</HintPath>
      <Private>False</Private>
    </Reference>
    <Reference Include="Gurren Core">
      <HintPath>F:\Program Files (x86)\Steam\steamapps\common\BloonsTD6\Mods\Gurren Core.dll</HintPath>
    </Reference>
    <Reference Include="Il2Cppmscorlib">
      <HintPath>F:\Program Files (x86)\Steam\steamapps\common\BloonsTD6\MelonLoader\Managed\Il2Cppmscorlib.dll</HintPath>
      <Private>False</Private>
    </Reference>
    <Reference Include="MelonLoader.ModHandler">
      <HintPath>F:\Program Files (x86)\Steam\steamapps\common\BloonsTD6\MelonLoader\MelonLoader.ModHandler.dll</HintPath>
      <Private>False</Private>
    </Reference>
    <Reference Include="Newtonsoft.Json, Version=6.0.0.0, Culture=neutral, PublicKeyToken=30ad4fe6b2a6aeed, processorArchitecture=MSIL">
      <SpecificVersion>False</SpecificVersion>
      <HintPath>F:\Program Files (x86)\Steam\steamapps\common\BloonsTD6\MelonLoader\Managed\Newtonsoft.Json.dll</HintPath>
      <Private>False</Private>
    </Reference>
    <Reference Include="System" />
    <Reference Include="System.Core" />
    <Reference Include="System.Xml.Linq" />
    <Reference Include="System.Data.DataSetExtensions" />
    <Reference Include="Microsoft.CSharp" />
    <Reference Include="System.Data" />
    <Reference Include="System.Net.Http" />
    <Reference Include="System.Xml" />
    <Reference Include="UnhollowerBaseLib">
      <HintPath>F:\Program Files (x86)\Steam\steamapps\common\BloonsTD6\MelonLoader\Managed\UnhollowerBaseLib.dll</HintPath>
      <Private>False</Private>
    </Reference>
    <Reference Include="UnityEngine.CoreModule">
      <HintPath>F:\Program Files (x86)\Steam\steamapps\common\BloonsTD6\MelonLoader\Managed\UnityEngine.CoreModule.dll</HintPath>
      <Private>False</Private>
    </Reference>
  </ItemGroup>
  <ItemGroup>
    <Compile Include="AntiCheat\CoopHandler.cs" />
    <Compile Include="AntiCheat\OdysseyHandler.cs" />
    <Compile Include="Enums\MathType.cs" />
    <Compile Include="Guard.cs" />
    <Compile Include="MelonMain.cs" />
    <Compile Include="Patches\Bloon_Initialise.cs" />
    <Compile Include="Patches\CoopButtonChecker_OnClick.cs" />
    <Compile Include="Patches\MainMenuEventPanel_OpenRaceEventScreen.cs" />
    <Compile Include="Patches\MainMenu_OnEnable.cs" />
    <Compile Include="Patches\OdysseyEventScreen_Update.cs" />
    <Compile Include="TowerModifier.cs" />
    <Compile Include="Patches\TowerSelectionMenu_UpdateHeroBooster.cs" />
    <Compile Include="Properties\AssemblyInfo.cs" />
    <Compile Include="AntiCheat\RaceHandler.cs" />
    <Compile Include="Serializer.cs" />
    <Compile Include="SessionData.cs" />
    <Compile Include="Settings.cs" />
  </ItemGroup>
  <ItemGroup />
  <Import Project="$(MSBuildToolsPath)\Microsoft.CSharp.targets" />
  <PropertyGroup>
    <PostBuildEvent>copy "$(TargetDir)$(TargetFileName)" "F:\Program Files (x86)\Steam\steamapps\common\BloonsTD6\Mods" /y</PostBuildEvent>
  </PropertyGroup>
</Project>

