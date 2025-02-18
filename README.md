# Create a .NET class library using Visual Studio Code


## dotnet 指令
* ### 查看 dotnet 版本
    ```console
    dotnet --version
    ```
* ### Create a solution
    * #### 建立範本「方案檔」
        ```console
        dotnet new sln
        ```
* ### Create a class library project
    * #### 建立範本「類別庫」
        * 第一種
            ```console
            dotnet new classlib -o StringLibrary
            ```
        * 第二種
            ```console
            dotnet new classlib --output StringLibrary
            ```
    * #### 新增專案 `StringLibrary\StringLibrary.csproj` 至解決方案
        ```console
        dotnet sln add StringLibrary/StringLibrary.csproj
        ```
    * #### 編譯
        ```console
        dotnet build
        ```
* ### Add a console app to the solution
    * #### 建立範本「主控台應用程式」
        ```console
        dotnet new console -o ShowCase
        ```
    * #### 新增專案 `ShowCase\ShowCase.csproj` 至解決方案
        ```console
        dotnet sln add ShowCase/ShowCase.csproj
        ```
* ### Add a project reference
    * #### 新增參考 `..\StringLibrary\StringLibrary.csproj` 已新增至專案
        ```console
        dotnet add ShowCase/ShowCase.csproj reference StringLibrary/StringLibrary.csproj
        ```
* ### Run the app
    * #### 執行範本「主控台應用程式」
        ```console
        dotnet run --project ShowCase/ShowCase.csproj
        ```

---
## 參考資料
* [Tutorial: Create a .NET class library using Visual Studio Code](https://learn.microsoft.com/en-us/dotnet/core/tutorials/library-with-visual-studio-code?pivots=dotnet-8-0)