---
title: "Arrays"
ms.date: "03/30/2017"
ms.technology: dotnet-standard
helpviewer_keywords: 
  - "class library design guidelines [.NET Framework], arrays"
  - "arrays [.NET Framework], usage guidelines"
  - "empty arrays"
ms.assetid: 66a1b3d8-6f3f-4715-b235-e1ff95e32d8e
author: "rpetrusha"
ms.author: "ronpet"
---
# Arrays
**✓ DO** prefer using collections over arrays in public APIs. The [Collections](../../../docs/standard/design-guidelines/guidelines-for-collections.md) section provides details about how to choose between collections and arrays.  
  
 **X DO NOT** use read-only array fields. The field itself is read-only and can't be changed, but elements in the array can be changed.  
  
 **✓ CONSIDER** using jagged arrays instead of multidimensional arrays.  
  
 A jagged array is an array with elements that are also arrays. The arrays that make up the elements can be of different sizes, leading to less wasted space for some sets of data (e.g., sparse matrix) compared to multidimensional arrays. Furthermore, the CLR optimizes index operations on jagged arrays, so they might exhibit better runtime performance in some scenarios.  
  
 *Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*  
  
 *Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*  
  
## See Also  
 <xref:System.Array>  
 [Framework Design Guidelines](../../../docs/standard/design-guidelines/index.md)  
 [Usage Guidelines](../../../docs/standard/design-guidelines/usage-guidelines.md)
