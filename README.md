# Binary tree printer

Вы можете распечатать красивое двоичное дерево в консоли.
***

# Как использовать

Вам нужно создать экземпляр класса `printer`, который будет использоваться (например, `ConsolePrinterBTree`). 
Затем создайте экземпляр класса `BTree` и передайте ему `printer`
(*кстати, вы можете добавить свои собственные принтеры для другой печати для дерева*).
Затем добавьте значения и распечатайте их.

(**File: BTree.cpp**)
```c++
#include "BTree.h"
#include "ConsolePrinterBTree.h"

int main()
{
   int arr[] = { 7,5,6,8,2,9 };
   int len = sizeof(arr) / sizeof(int);
   PrinterBTree<int>* printer = new ConsolePrinterBTree<int>();
   BTree<int> tree = BTree<int>(printer);
   for (int i = 0; i < len; i++)
   {
      tree.AddNode(arr[i]);
   }
   tree.Print();
}
```

<img width="200" alt="image" src="https://user-images.githubusercontent.com/78900834/182572101-e9625f55-80d7-41c2-8665-a07e664390df.png">
