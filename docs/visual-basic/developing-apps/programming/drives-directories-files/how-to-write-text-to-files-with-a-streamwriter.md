---
title: 如何：使用 StreamWriter 向文件中写入文本
ms.date: 07/20/2015
helpviewer_keywords:
- files [Visual Basic], writing to
- text, writing to files
- writing to files [Visual Basic], StreamWriter
ms.assetid: 99762e57-ef46-4dcc-8959-a8f79c22f067
ms.openlocfilehash: 869e29263abcdd8525b2c372c7bb466e3e21fc65
ms.sourcegitcommit: 7588136e355e10cbc2582f389c90c127363c02a5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/15/2020
ms.locfileid: "74334502"
---
# <a name="how-to-write-text-to-files-with-a-streamwriter-in-visual-basic"></a>如何：在 Visual Basic 中使用 StreamWriter 向文件中写入文本

此示例将通过 <xref:System.IO.StreamWriter> 方法打开 `My.Computer.FileSystem.OpenTextFileWriter` 对象，并会使用该对象和 <xref:System.IO.TextWriter.WriteLine%2A> 类的 <xref:System.IO.StreamWriter> 方法向文本文件写入字符串。  
  
## <a name="example"></a>示例  

 [!code-vb[VbFileIOWrite#5](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbFileIOWrite/VB/Class1.vb#5)]  
  
## <a name="robust-programming"></a>可靠编程  

 以下情况可能会导致异常：  
  
- 文件存在且为只读 (<xref:System.IO.IOException>)。  
  
- 磁盘已满 (<xref:System.IO.IOException>)。  
  
- 路径名称过长 (<xref:System.IO.PathTooLongException>)。  
  
## <a name="net-framework-security"></a>.NET Framework 安全性  

 此示例在文件尚未存在时创建新文件。 如果某个应用程序需要创建文件，则该应用程序需要针对文件夹的 `Create` 访问权限。 如果文件已存在，则该应用程序只需要 `Write` 访问权限（这是较弱的特权）。 如有可能，在部署过程中创建文件，并且仅授予针对单个文件的 `Read` 访问权限（而不是针对 `Create` 文件夹的访问权限）会更加安全。  
  
## <a name="see-also"></a>另请参阅

- <xref:System.IO.StreamWriter>
- <xref:Microsoft.VisualBasic.FileIO.FileSystem.OpenTextFileWriter%2A>
- [如何：读取文本文件](../../../../visual-basic/developing-apps/programming/drives-directories-files/how-to-read-from-text-files.md)
- [写入文件](../../../../visual-basic/developing-apps/programming/drives-directories-files/writing-to-files.md)
