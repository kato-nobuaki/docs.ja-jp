---
redirect_url: /dotnet/articles/csharp/linq/query-a-collection-of-objects
caps.handback.revision: 8
---
# 方法 : オブジェクトのコレクションを照会する (C# プログラミング ガイド)
この例では、`Student` オブジェクトのリストに対して簡単なクエリを実行する方法を示します。  各 `Student` オブジェクトには、生徒についての基本情報と 4 回の試験のその生徒の得点を表すリストが含まれます。  
  
 このアプリケーションは、同じ `students`  データ ソースを使用する、このセクションのその他の多くの例のフレームワークとなるものです。  
  
## 使用例  
 次のクエリでは、1 回目の試験で 90 点以上得点した生徒が返されます。  
  
 [!code-cs[csProgGuideLINQ#15](../../../csharp/programming-guide/arrays/codesnippet/CSharp/how-to-query-a-collection-of-objects_1.cs)]  
  
 このクエリは、実際に試すことができるように意図的にシンプルにしてあります。  たとえば、`where` 句でその他の述語を試したり、`orderby` 句を使用して結果を並べ替えたりできます。  
  
## コードのコンパイル  
  
-   .NET Framework Version 3.5 を対象とする [!INCLUDE[vs_current_short](../../../csharp/programming-guide/classes-and-structs/includes/vs-current-short-md.md)] プロジェクトを作成します。  既定では、プロジェクトには、System.Core.dll への参照と、System.Linq 名前空間に対する `using` ディレクティブが含まれます。  
  
-   コードをプロジェクト内にコピーします。  
  
-   F5 キーを押して、プログラムをコンパイルおよび実行します。  
  
-   任意のキーを押して、コンソール ウィンドウを終了します。  
  
## 参照  
 [LINQ クエリ式](../../../csharp/programming-guide/linq-query-expressions/index.md)