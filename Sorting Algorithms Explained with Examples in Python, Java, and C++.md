# Sorting Algorithms Explained with Examples in Python, Java, and C++

![Sorting Algorithms Explained with Examples in Python, Java, and C++](https://www.freecodecamp.org/news/content/images/size/w2000/2021/06/5f9c9ede740569d1a4ca3f9d-1.jpg)

## ما هي خوارزميات الترتيب (Sorting Algorithms)؟
خوارزميات الترتيب (Sorting Algotihms) هي مجموعة من التعليمات التي تستقبل مصفوفه (array) و ترتبهم بترتيب معين.

الترتيب أكثر شيوعا بطريقه رقمية (numerical) أو حسب الحروف الأبجدية (alphabetical or lexicographical) ويمكن أن يكون تصاعديا أو تنازليا. 

## ما أهمية خوارزميات الترتيب ؟
حيث أن الترتيب في كثير من الأحوال يمكن أن يقلل من تعقيد المشكلة ، فهو من أهم الخوارزميات في علوم الكمبيوتر ، وهذه الخوارزميات لها تطبيق مباشر في خوارزميات البحث ( Searching Algorithms )،و خوارزميات قواعد البيانات ( Database Algorithms)  ،و (Devide and Conquer)،و هياكل البيانات (Data structures Algorithms) و الكثير غير ذلك

### المفاضلة (Trade-Offs) بين الخوارزميات
عند استخدام خوارزميات مختلفه بعض الأسئلة يجب أن تسأل. ما حجم المجموعة (collection) التي يتم ترتيبها؟ ما حجم الذاكرة المتاحة للاستخدام؟ هل يمكن أن يزيد حجم المجموعة؟

الإجابة على هذه الأسئلة يمكن أن يحدد أي خوارزمية ستكون الأفضل في هذا الموقف. بعض الخوارزميات مثل Merge sort يمكن أن تحتاج مساحة كبيرة من الذاكرة لتعمل، بينما Insertion sort ليس دائما الأسرع لكنه لا يحتاج الكثير من الموارد ليعمل.

يجب أولا تحديد متطلبات النظام و قيوده قبل أن تقرر أي الخوارزميات سوف تستخدم. 

## بعض خوارزميات الترتيب الأكثر شيوعا
بعض من خوارزميات الترتيب الأكثر شيوعا :-
-   Selection Sort
-   Bubble Sort
-   Insertion Sort
-   Merge Sort
-   Quick Sort
-   Heap Sort
-   Counting Sort
-   Radix Sort
-   Bucket Sort

لكن قبل أن نبدأ في أيا منهم، هيا نتعلم قليلا عن كيفية تصنيف خوارميات الترتيب. 

### تصنيف خوارزميات الترتيب

خوارزميات الترتيب يمكن أن تصنف بناء على المعاملات الآتيه :

1.بناء على عدد التبديلات (Swaps) وهو عدد المرات التي تقوم فيها الخوارزمية بتبديل مكان عنصرين في المجموعة لترتيبها. `Selection Sort` يتطلب أقل عدد من التبديلات.

2.بناء على عدد المقارنات (Comparisons) و هو عدد المرات التي تقوم فيها الخوارزمية بمقارنة عناصر بأخرى لترتيب المجموعة.باستخدام [Big-O notation](https://guide.freecodecamp.org/computer-science/notation/big-o-notation/), أمثلة خوارزميات الترتيب المذكورة بالأعلى تطلب على الأقل `O(nlogn)` مقارنة في أفضل حالة(Best case) و `O(n^2)` مقارنة في أسوء حالة (worst case) لمعظم المخرجات (outputs).

3.بناء على استخدامها للـ Recursion أو عدم استخدامه Non-Recursion بعض خوارزميات الترتيب ، مثل `Quick Sort` ، تستخدم  Recursive techniques  لترتيب المدخلات. البعض الآخر مثل `Selection Sort` أو  `Insertion Sort` ، تستخدم Non-Recursive techniques. واخيرا، بعض خوارزميات الترتيب مثل `Merge Sort` تستخدم  الأسلوبين معا  Recursive techniques بالإضافة إلى Non-Recursive techniques لترتيب المدخلات.

4.بناء على الثبات (Stability) خوارزميات الترتيب تعتبر  `stable` عندما تحافظ الخوارزمية على الترتيب النسبي للعناصر التي تملك Keys متساوية. بعبارة أخرى، عند وجود عنصران متساويان فإنهم يحافظان على ترتيبهم بعد عملية الترتيب كما كانوا قبل عملية الترتيب (مثال:إذا كان (عنصر أ   =  عنصر ب)  وعنصر أ يظهر في المجموعة الأصلية قبل الترتيب قبل عنصر ب فإنه يظهر في المجموعة النهائية بعد الترتيب قبل عنصر ب).

5.`Insertion Sort` ،و  `Merge Sort` ،و  `Bubble Sort` يصنفوا كـ stable.

6.`Quick Sort`،و `Heap Sort`  يصنفوا كـ not stable

7.بناء على متطلبات الذاكرة الإضافية خوارزميات الترتيب يمكن أن تصنف كـ  `in place` عندما تطلب مساحة إضافية ثابتة من الذاكرة   `O(1)` للقيام بعملية الترتيب

8.`Insertion Sort` و`Quick Sort` يصنفوا كـ `in place`  sort  حيث أنها تنقل العناصر حول Pivot ولا تستخدم  مصفوفة (array) منفصلة على عكس Merge sort  حيث حجم مجموعة المدخلات (input) يجب أن يكون محدد مسبقا لتخزين المخرجات (output) أثناء عملية الترتيب

9.`Merge Sort` مثال على `out place`  sort  حيث يتطلب ذاكرة إضافية لإتمام عملياته 

### أفضل time complexity ممكنة لأي خوارزمية ترتيب تعتمد على المقارنة (comparison)

أي خوارزمية ترتيب تعتمد على المقارنة  يمكن على الأقل أن تصل إلى  nLog2n مقارنة  لترتيب مصفوفة المدخلات (input array) ,  Heapsort  و  merge sort يعتبروا asymptotically optimal كخوارزميات مقارنة. وهذا يمكن إثباته بسهولة عن طريق رسم decision tree diagram لهما. 

## Bucket Sort

Bucket Sort  هو  خوارزمية  ترتيب تعتمد على المقارنة و التي تعمل على مجموعة من العناصر بتقسيمهم إلى buckets مختلفة و ترتيب كل  من هذه الـ buckets على حدى. كل bucket يتم ترتيب عناصره على حدى اما باستخدام خوارزمية ترتيب مختلفة او بتطبيق bucket sort مره اخرى recursively.

Bucket Sort  يستخدم بشكل رئيسي عندما تكون المدخلات (inputs) موزعه على نطاق محدد  (uniformly distributed over a range) .

### افترض أن المشكلة التالية تواجهك

تم اعطائك  مصفوفة (array) كبيرة من الأرقام العشرية (Floating point integers) والتي تقع بين حد أدنى و أقصى محددين . وهذه المصفوفة تحتاج للترتيب.

الطريقة الأبسط لحل هذه المشكلة هي استخدام خواريزمية ترتيب اخرى مثل Merge sort ،أو Heap sort ،أو Quick sort مع ذلك هذه الخوارزميات تضمن لك في أفضل حالة best case time complexity of O(NlogN) ، ولكن bucket sort يمكن أن يؤدي هذه المهمة في O(N)time .

هيا نأخذ نظرة أقرب عنه.

اعتبر انك تحتاج لانشاء مصفوفة من القوائم (array of lists) لتمثيل الـ Buckets. الآن يجب إدراج العناصر في هذه ال Buckets بناء على خصائصهم.و من ثم يمكن ترتيب عناصر كل Bucket على حدى باستخدام Insertion sort. 

### Pseudo Code for Bucket Sort:

```
void bucketSort(float[] a,int n)

{

    for(each floating integer 'x' in n)

    {
        insert x into bucket[n*x]; 
    }

    for(each bucket)

    {
        sort(bucket);
    }

}

```

## Counting Sort

counting sort هو أسلوب للترتيب يعتمد على وجود مفاتيح العناصر (Keys) في نطاق محدد. ويعمل عن طريق حساب عدد الكائنات (Objects) التي تمتلك مفاتيح عناصر (Keys) فريدة (تعتبر مثل الـhashing)  ومن ثم إجراء بعض العمليات الحسابية لحساب مكان كل كائن في مجموعة المخرجات (output). 

### أمثلة:

```
للتبسيط سوف نعتبر أن البيانات تقع في نطاق من 0 إلى 9
المدخلات: 1,4,1,2,7,5,2
  1) أنشئ مصفوفة العد (Counting array) لتخزين مرات تكرار كل كائن.
  Index:     0  1  2  3  4  5  6  7  8  9
  Count:     0  2  2  0  1  1  0  1  0  0

  2)قم بتعديل مصفوفة العد ليكون كل عنصر عند كل Index يساوي مجموع كل الأعداد السابقة. 
  Index:     0  1  2  3  4  5  6  7  8  9
  Count:     0  2  4  4  5  6  6  7  7  7

مصفوفة العد الناتجة تحدد مكان كل كائن في مصفوفة المخرجات

3) اخراج كل كائن من مصفوفة المدخلات الى المجموعة المرتبة يكون متبوع بـ
تقليل قيمته في مصفوفة العد بمقدار 1
معالجة مجموعة المدخلات : 1,4,1,2,7,5,2 ترتيب 1 في المخرجات هو 2 
ضع 1 في index 2 في المخرجات (outputs).ثم قلل قيمته في مصفوفة العد بمقدار 1
ليتم تخزين ال 1 الاخر في ال index السابق له
  

```


### الخصائص

-   Space complexity: O(K)
-   Best case performance: O(n+K)
-   Average case performance: O(n+K)
-   Worst case performance: O(n+K)
-   Stable: Yes (K هو عدد العناصر الفريدة في ال array)

### Implementation in JavaScript

```js
let numbers = [1, 4, 1, 2, 7, 5, 2];
let count = [];
let i, z = 0;
let max = Math.max(...numbers);      
// initialize counter
for (i = 0; i <= max; i++) {
    count[i] = 0;
}
for (i=0; i < numbers.length; i++) {
    count[numbers[i]]++;
}
for (i = 0; i <= max; i++) {
    while (count[i]-- > 0) {
        numbers[z++] = i;
    }
}
// output sorted array
for (i=0; i < numbers.length; i++) {
    console.log(numbers[i]);
}

```

### C++ Implementation

```cpp
#include <iostream>

void countSort(int upperBound, int lowerBound, std::vector<int> numbersToSort) //lower and upper bounds of numbers in vector
{
  int range = upperBound - lowerBound;                  //create a range large enough to get every number between the min and max
  std::vector<int> counts (range);                      //initialize of counts of the size of the range
  std::fill(counts.begin(), counts.end(), 0);           //fill vector of zeros
  
  for (int i = 0; i < numbersToSort.size(); i++)
  {
      int index = numbersToSort[i] - lowerBound; //For example, if 5 is the lower bound and numbersToSort[i] is 5. index will be 0 and the       counts[index]+= 1;                         //count of 5 will be stored in counts[0]
  }
  
  std::cout << counts << std::endl;
} 

```

### Swift Implementation

```swift
func countingSort(_ array: [Int]) {
  // Create an array to store the count of each element
  let maxElement = array.max() ?? 0
  var countArray = [Int](repeating: 0, count: Int(maxElement + 1))
  
  for element in array {
    countArray[element] += 1
  }
  var z = 0
  var sortedArray = [Int](repeating: 0, count: array.count)

  for index in 1 ..< countArray.count {
    //print index element required number of times
    while countArray[index] > 0 {
      sortedArray[z] = index
      z += 1
      countArray[index] -= 1
    }
  }
  
  print(sortedArray)
}

```

## Insertion Sort

Insertion sort هو خوارزمية ترتيب بسيطة لعدد صغير من العناصر
### مثال:

في Insertion sort، نقوم بقارنة العنصر الحالي  `key` مع العناصر السابقة له. في حال كانت العناصر السابقة له أكبر منه. نقوم بنقل العنصر السابق مكان واحد للأمام 

بداية من المكان الأول (index 1) إلى نهاية مصفوفة المدخلات.

[ 8 3 5 1 4 2 ]

الخطوة الأولى :

 



```
 key=3  //بداية من العنصر في  1st index.

هنا `key` سيتم مقارته بالعناصر السابقة له.

في هذه الحالة، `key` سيتم مقارنته مع 8. وبما أن  8 > 3 ، سيتم نقل العنصر 8 مكان للأمام 
ومن ثم وضع `key` في المكان السابق له.
النتيجة: [ 3 8 5 1 4 2 ]

```

الخطوة الثانية:
![[ 3 8 5 1 4 2 ]](https://github.com/blulion/freecodecamp-resource/blob/master/insertion_sort/2.png?raw=true)

```
Key = 5 //2nd index

8 > 4 // قم بنقل 8 إلى  2nd index ثم ضع 5 في 1st index.

النتيجة: [ 3 5 8 1 4 2 ]
```

الخطوة الثالثة:
![[ 3 5 8 1 4 2 ]](https://github.com/blulion/freecodecamp-resource/blob/master/insertion_sort/3.png?raw=true)

```
      key = 1 //3rd index

      8 > 1     => [ 3 5 1 8 4 2 ]  

      5 > 1     => [ 3 1 5 8 4 2 ]

      3 > 1     => [ 1 3 5 8 4 2 ]

      النتيجة: [ 1 3 5 8 4 2 ]

```

الخطوة الرابعة:
![[ 1 3 5 8 4 2 ]](https://github.com/blulion/freecodecamp-resource/blob/master/insertion_sort/4.png?raw=true)

```
      key = 4 //4th index

      8 > 4   => [ 1 3 5 4 8 2 ]

      5 > 4   => [ 1 3 4 5 8 2 ]

      3 > 4   ≠>  توقف

      النتيجة: [ 1 3 4 5 8 2 ]

```

الخطوة الخامسة:
![[ 1 3 4 5 8 2 ]](https://github.com/blulion/freecodecamp-resource/blob/master/insertion_sort/5.png?raw=true)

```
      key = 2 //5th index

      8 > 2   => [ 1 3 4 5 2 8 ]

      5 > 2   => [ 1 3 4 2 5 8 ]

      4 > 2   => [ 1 3 2 4 5 8 ]

      3 > 2   => [ 1 2 3 4 5 8 ]

      1 > 2   ≠> توقف

      النتيجة: [1 2 3 4 5 8]

```

![[ 1 2 3 4 5 8 ]](https://github.com/blulion/freecodecamp-resource/blob/master/insertion_sort/6.png?raw=true)

الخوارزمية الموضحة بالأسفل هي نسخة محسنة قليلا (optimized) لتفادي تغيير مكان `key`  element في كل دورة (iteration). بدلا من ذلك  سيتم تغيير مكانه مره واحدة في نهاية كل دورة iteration (step).

```
    InsertionSort(arr[])
      for j = 1 to arr.length
         key = arr[j]
         i = j - 1
         while i > 0 and arr[i] > key
            arr[i+1] = arr[i]
            i = i - 1
         arr[i+1] = key

```

تنفيذ الخوارزمية (implementation) بلغة JavaScript: 
```js
function insertion_sort(A) {
    var len = array_length(A);
    var i = 1;
    while (i < len) {
        var x = A[i];
        var j = i - 1;
        while (j >= 0 && A[j] > x) {
            A[j + 1] = A[j];
            j = j - 1;
        }
        A[j+1] = x;
        i = i + 1;
    }
}

```

تنفيذ  (implementation) آخر سريع بلغة swift:
```swift
  var array = [8, 3, 5, 1, 4, 2]

  func insertionSort(array:inout Array<Int>) -> Array<Int>{
      for j in 0..<array.count {
          let key = array[j]
          var i = j-1

          while (i > 0 && array[i] > key){
              array[i+1] = array[i]
              i = i-1
          }
          array[i+1] = key
      }
      return array
  }

```

وهذا باستخدام لغة Java:
```java
public int[] insertionSort(int[] arr)
      for (j = 1; j < arr.length; j++) {
         int key = arr[j]
         int i = j - 1
         while (i > 0 and arr[i] > key) {
            arr[i+1] = arr[i]
            i -= 1
         }
         arr[i+1] = key
      }
      return arr;

```

ولغة C...
```c
void insertionSort(int arr[], int n) 
{ 
   int i, key, j; 
   for (i = 1; i < n; i++) 
   { 
       key = arr[i]; 
       j = i-1;
       while (j >= 0 && arr[j] > key) 
       { 
           arr[j+1] = arr[j]; 
           j = j-1; 
       } 
       arr[j+1] = key; 
   } 
} 

```

### الخصائص:

-   Space Complexity: O(1)
-   Time Complexity: O(n), O(n* n), O(n* n) for Best, Average, Worst cases respectively.
-   Best Case: المصفوفة(array) مرتبة مسبقا
-   Average Case: المصفوفة(array) مرتبة عشوائيا
-   Worst Case: المصفوفة(array) معكوسة الترتيب.
-   Sorting In Place: Yes
-   Stable: Yes

## Heapsort

Heapsort هو خوارزمية ترتيب فعالة يعتمد على استخدام min/max heap. و Heap هو أحد هياكل البيانات (Data structures) التي تعتمد على Tree والتي توفر خصائص الـ Heap - وهذه الخصائص بالنسبة لـ Max heap،أن يكون الـ Key لأي نقطة (node) أصغر من أو يساوي  الـ Key للـ parent الخاص بها (إذا امتلكت واحدا).

وهذه الخصائص يمكن استخدامها للوصول لأكبر عنصر في ال Heap في وقت  O(logn) time باستخدام خاصية maxHeapify. وهذه العملية يتم تنفيذها n من المرات، في كل مرة يتم نقل أكبر عنصر في الـ Heap إلى أول مكان فيه (Top) ومن ثم استخراجه منه إلى مصفوفة مرتبة (sorted array). وبالتالي بعد n دورات سيكون لدينا نسخة مرتبة من المدخلات.

الخوارزمية ليست in-place algorithm وتحتاج لانشاء Heab data structure أولا. أيضا هذه الخوارزمية  unstable، مما يعني أنه عند مقارنة عنصرين لهما نفس الـ Key الترتيب الأصلي لهما يمكن أن يتغير. 

تعمل الخوارزمية في O(nlogn) time وتحتاج O(1) مساحة إضافية [O(n) إذا وضعنا في الاعتبار المساحة المطلوبة لتخزين البيانات المدخلة (inputs)] حيث كل العمليات يتم تنفيذها بالكامل in-place.

The best, worst and average case time complexity of Heapsort is O(nlogn).وعلى الرغم من  أن Heap sort يمتلك worse-case complexity أفضل من quicksort، فإن quicksort منفذ جيدا (well-implemented) يعمل بشكل أسرع عمليا. أيضا هذه خوارزمية معتمدة على المقارنة (comparison-based algorithm) فبالتالي يمكن استخدامها لترتيب البيانات الغير عدددية  الى حد ما حيث بعض الخصائص (Heap property) يمكن تعريفها بناء على العناصر. 

An implementation in Java موضح بالأسفل :

```java
import java.util.Arrays;
public class Heapsort {

	public static void main(String[] args) {
		//test array
		Integer[] arr = {1, 4, 3, 2, 64, 3, 2, 4, 5, 5, 2, 12, 14, 5, 3, 0, -1};
		String[] strarr = {"hope you find this helpful!", "wef", "rg", "q2rq2r", "avs", "erhijer0g", "ewofij", "gwe", "q", "random"};
		arr = heapsort(arr);
		strarr = heapsort(strarr);
		System.out.println(Arrays.toString(arr));
		System.out.println(Arrays.toString(strarr));
	}
	
	//O(nlogn) TIME, O(1) SPACE, NOT STABLE
	public static <E extends Comparable<E>> E[] heapsort(E[] arr){
		int heaplength = arr.length;
		for(int i = arr.length/2; i>0;i--){
			arr = maxheapify(arr, i, heaplength);
		}
		
		for(int i=arr.length-1;i>=0;i--){
			E max = arr[0];
			arr[0] = arr[i];
			arr[i] = max;
			heaplength--;
			arr = maxheapify(arr, 1, heaplength);
		}
		
		return arr;
	}
	
	//Creates maxheap from array
	public static <E extends Comparable<E>> E[] maxheapify(E[] arr, Integer node, Integer heaplength){
		Integer left = node*2;
		Integer right = node*2+1;
		Integer largest = node;
		
		if(left.compareTo(heaplength) <=0 && arr[left-1].compareTo(arr[node-1]) >= 0){
			largest = left;
		}
		if(right.compareTo(heaplength) <= 0 && arr[right-1].compareTo(arr[largest-1]) >= 0){
			largest = right;
		}	
		if(largest != node){
			E temp = arr[node-1];
			arr[node-1] = arr[largest-1];
			arr[largest-1] = temp;
			maxheapify(arr, largest, heaplength);
		}
		return arr;
	}
}

```

Implementation in C++

```cpp
#include <iostream>
using namespace std;
void heapify(int arr[], int n, int i) 
{ 
    int largest = i; 
    int l = 2*i + 1;  
    int r = 2*i + 2;
    if (l < n && arr[l] > arr[largest]) 
        largest = l;
    if (r < n && arr[r] > arr[largest]) 
        largest = r;
    if (largest != i) 
    { 
        swap(arr[i], arr[largest]); 
  
        
        heapify(arr, n, largest); 
    } 
} 
  
 
void heapSort(int arr[], int n) 
{ 
    
    for (int i = n / 2 - 1; i >= 0; i--) 
        heapify(arr, n, i); 
  
    
    for (int i=n-1; i>=0; i--) 
    { 

        swap(arr[0], arr[i]); 
  
        
        heapify(arr, i, 0); 
    } 
} 
void printArray(int arr[], int n) 
{ 
    for (int i=0; i<n; ++i) 
        cout << arr[i] << " "; 
    cout << "\n"; 
} 
int main() 
{ 
    int arr[] = {12, 11, 13, 5, 6, 7}; 
    int n = sizeof(arr)/sizeof(arr[0]); 
  
    heapSort(arr, n); 
  
    cout << "Sorted array is \n"; 
    printArray(arr, n); 
}

```

## Radix Sort
متطلبات مسبقة: counting sort.

quickSort,mergeSort,heapSort هم خورارزميات ترتيب تعتمد على المقارنة (comparison-based). لكن هذا ليس الحال مع  CountSort. حيث يملك  complexity of O(n+k) حيث k هو أكبر عنصر في مصفوفة المدخلات (inputs). وبالتالي إذا كان K يساوي O(n) يصبح CountSort خواريزمية ترتيب خطية (linear sorting)، وبالتالي أفضل من خوارزميات المقارنة (comparison) التي تمتلك O(nlogn) time complexity 

### الخوارزمية:
لكل رقم i حيث i يتراوح من الرقم الأقل قيمة ( least significant digit) إلى الرقم الأعلى قيمة  ( most significant digit) من عدد، يستخدم CountSort  لترتيب مصفوفة المدخلات (input array)  بناء على الرقم i  أو  ith digit،  يستخدم CountSortلأنه يصنف كـ stable. 

مثال:اعتبر أن مصفوفة المدخلات (input array) هي

10, 21, 17, 34, 44, 11, 654, 123

بناء على الخوارزمية، سوف نقوم بترتيب المدخلات  بناء على الرقم الأول أو الآحاد (one's digit)  وهو الرقم الأقل قيمة (least significant digit).

0: 10  
1: 21 11  
2:  
3: 123  
4: 34 44 654  
5:  
6:  
7: 17  
8:  
9:

وبالتالي تصبح المصفوفة: 10, 21, 11, 123, 24, 44, 654, 17.

والآن سنرتبهم بناء على الرقم الثاني أو العشرات (ten's digit)

0:  
1: 10 11 17  
2: 21 123  
3: 34  
4: 44  
5: 654  
6:  
7:  
8:  
9:

وبالتالي تصبح المصفوفة : 10, 11, 17, 21, 123, 34, 44, 654.

و اخيرا نقوم بترتيبهم بناء على الرقم الثالث أو المئات ( hundred's digit) وهو الرقم الأعلى قيمة (most significant digit).

0: 010 011 017 021 034 044  
1: 123  
2:  
3:  
4:  
5:  
6: 654  
7:  
8:  
9:

وبالتالي تصبح المصفوفة : 10, 11, 17, 21, 34, 44, 123, 654  وهي مرتبة.هذه هي الطريقة التي تعمل بها الخوارزمية.

An implementation in C:

```c
void countsort(int arr[],int n,int place){

        int i,freq[range]={0};         //range for integers is 10 as digits range from 0-9
        int output[n];

        for(i=0;i<n;i++)
                freq[(arr[i]/place)%range]++;

        for(i=1;i<range;i++)
                freq[i]+=freq[i-1];
        
        for(i=n-1;i>=0;i--){
                output[freq[(arr[i]/place)%range]-1]=arr[i];
                freq[(arr[i]/place)%range]--;
        }
        
        for(i=0;i<n;i++)
                arr[i]=output[i];
}

void radixsort(ll arr[],int n,int maxx){            //maxx is the maximum element in the array

        int mul=1;
        while(maxx){
                countsort(arr,n,mul);
                mul*=10;
                maxx/=10;
        }
}

```

## Selection Sort

Selection Sort يعتبر من أبسط خوارزميات الترتيب. و قد اكتسب اسمه من الطريقة التي يعمل بها في الترتيب، حيث يختار (select) أصغر عنصر في المصفوفة وينقله إلى مكانه.

وهذه هي الطريقة التي يعمل بها:

1. حدد أصغر عنصر في المصفوفة(array) وبدله مع العنصر الأول فيها.
2. حدد ثاني أصغر عنصر وبدله مع ثاني عنصر في المصفوفة.
3. حدد ثالث أصغر عنصر وبدله مع ثالث عنصر في المصفوفة.
4. كرر عملية إيجاد العنصر الأصغر التالي وابدال مكانه ليكون في المكان المناسب حتى تصبح المصفوفة بالكامل مرتبة.

ولكن كيف تكتب الكود المناسب لإيجاد مكان (index) ثاني أصغر عنصر في المصفوفة ؟

أحد الطرق البسيطة هي ملاحظة أن أصغر عنصر تم وضعه في index 0 ، وبالتالي تم تصغير حجم المشكلة لإيجاد أصغر عنصر في المصفوفة بداية من index 1.

Selection sort دائما ما يقوم بنفس عدد المقارنات لكل Key وهي N(N − 1)/2. 

### Implementation in C/C++
البرنامج التالي لغة C++ يحتوي على تنفيذ (Implementation)  لـ Selection Sort بطريقتين  iterative و   recursive وكلاهما تم استدعائه في `main()`  function.

```cpp
#include <iostream>
#include <string>
using namespace std;

template<typename T, size_t n>
void print_array(T const(&arr)[n]) {
    for (size_t i = 0; i < n; i++)
        std::cout << arr[i] << ' ';
    cout << "\n";
}

int minIndex(int a[], int i, int j) {
    if (i == j)
        return i;
    int k = minIndex(a, i + 1, j);
    return (a[i] < a[k]) ? i : k;
}

void recurSelectionSort(int a[], int n, int index = 0) {
    if (index == n)
        return;
    int k = minIndex(a, index, n - 1);
    if (k != index)
        swap(a[k], a[index]);
    recurSelectionSort(a, n, index + 1);
}

void iterSelectionSort(int a[], int n) {
    for (int i = 0; i < n; i++)
    {
        int min_index = i;
        int min_element = a[i];
        for (int j = i + 1; j < n; j++)
        {
            if (a[j] < min_element)
            {
                min_element = a[j];
                min_index = j;
            }
        }
        swap(a[i], a[min_index]);
    }
}

int main() {
    int recurArr[6] = { 100,35, 500, 9, 67, 20 };
    int iterArr[5] = { 25, 0, 500, 56, 98 };

    cout << "Recursive Selection Sort"  << "\n";
    print_array(recurArr); // 100 35 500 9 67 20
    recurSelectionSort(recurArr, 6);
    print_array(recurArr); // 9 20 35 67 100 500

    cout << "Iterative Selection Sort" << "\n";
    print_array(iterArr); // 25 0 500 56 98
    iterSelectionSort(iterArr, 5);
    print_array(iterArr); // 0 25 56 98 500
}

```

### Implementation in JavaScript

```js
function selection_sort(A) {
    var len = A.length;
    for (var i = 0; i < len - 1; i = i + 1) {
        var j_min = i;
        for (var j = i + 1; j < len; j = j + 1) {
            if (A[j] < A[j_min]) {
                j_min = j;
            } else {}
        }
        if (j_min !== i) {
            swap(A, i, j_min);
        } else {}
    }
}

function swap(A, x, y) {
    var temp = A[x];
    A[x] = A[y];
    A[y] = temp;
}

```

### Implementation in Python

```ps
def seletion_sort(arr):
         if not arr:
         return arr
    for i in range(len(arr)):
         min_i = i
         for j in range(i + 1, len(arr)):
              if arr[j] < arr[min_i]:
                  min_i = j
         arr[i], arr[min_i] = arr[min_i], arr[i]

```

### Implementation in Java

```java
public void selectionsort(int array[])
{
    int n = array.length;            //method to find length of array 
    for (int i = 0; i < n-1; i++)
    {
        int index = i;
        int min = array[i];          // taking the min element as ith element of array
        for (int j = i+1; j < n; j++)
        {
            if (array[j] < array[index])
            {
                index = j;
                min = array[j];
            }
        }
        int t = array[index];         //Interchange the places of the elements
        array[index] = array[i];
        array[i] = t;
    }
}

```

### Implementation in MATLAB

```
function [sorted] = selectionSort(unsorted)
    len = length(unsorted);
    for i = 1:1:len
        minInd = i;
        for j = i+1:1:len
           if unsorted(j) < unsorted(minInd) 
               minInd = j;
           end
        end
        unsorted([i minInd]) = unsorted([minInd i]);    
    end
    sorted = unsorted;
end

```

### Properties

-   Space Complexity: **O(n)**
-   Time Complexity: **O(n2)**
-   Sorting in Place: **Yes**
-   Stable: **No**

## Bubble Sort
بنفس الطريقة التي ترتفع بها الفقاعات من أسفل الكأس، `bubble sort` هو خوارزمية بسيطة لترتيب list ، عن طريق رفع أكبر قيم أو أصغر قيم إلى الأعلى مثل الفقاعات. الخوارزمية تمر (traverses) على list وتقارن القيم المتجاورة، وتقوم بتبديل أماكنهم  اذا لم يكونوا بالترتيب الصحيح.

مع worst-case complexity of O(n^2) ، يعتبر bubble sort بطئ جدا عند مقارنته بخوارزميات اخرى مثل Quick Sort. ولكن على الجانب الاخر يعتبر من أبسط الخوارزميات لفهمه أو كتابته من الصفر.

من منظور تقني، bubble sort  يستخدم في ترتيب مصفوفات صغيرة الحجم خاصة عند محاولة ترتيب مجموعة من العناصر على أجهزة كمبيوتر محدودة الذاكرة.

### مثال:

### أول دورة (pass) في المصفوفة:
* بداية من   `[4, 2, 6, 3, 9]`، تقوم الخوارزمية بمقارنة أول عنصرين في المصفوفة، 4و2 وتقوم بتبديلهم لأن 4>2 :  `[2, 4, 6, 3, 9]`
* في الخطوة التالية تقوم بقارنة العنصرين التاليين، 4و6 وتجدهم بالفعل مرتبين وتبقى `[2, 4, 6, 3, 9]`
* العنصريين التاليين يتم تبديلهم لأن 6>3 :    `[2, 4, 3, 6, 9]`
* العنصرين التاليين 6و9 بالفعل مرتبين لذا لا يتم تبديلهم 

### ثاني دورة (pass) في المصفوفة:

-   2 < 4, وبالتالي لا حاجة لتبديل أماكنهم:  `[2, 4, 3, 6, 9]`
-   الخوارزمية تقوم بتبديل العنصرين التاليين لأن 3 < 4:  `[2, 3, 4, 6, 9]`
-   لا حاجة لتبديلات لأن 4 < 6:  `[2, 3, 4, 6, 9]`
-   , 6 < 9, وبالتالي مرة اخرى لا حاجة للتبديل:  `[2, 3, 4, 6, 9]`
الـ List حاليا اصبحت مرتبة بالفعل، ولكن bubble sort لا يمكنه تمييز ذلك. وبالتالي يحتاج لإكمال دورة كاملة اخرى بدون اجراء أي تبديلات ليدرك أن الـ list مرتبة.

### ثالث دورة (pass) في المصفوفة:

-   `[2, 4, 3, 6, 9]`  =>  `[2, 4, 3, 6, 9]`
-   `[2, 4, 3, 6, 9]`  =>  `[2, 4, 3, 6, 9]`
-   `[2, 4, 3, 6, 9]`  =>  `[2, 4, 3, 6, 9]`
-   `[2, 4, 3, 6, 9]`  =>  `[2, 4, 3, 6, 9]`
من الواضح أن bubble sort بعيد جدا عن أن يكون أكفأ خوارزميات الترتيب. مع ذلك ، يمكنك بسهولة أن تنفذه بنفسك. 

#### Properties

-   Space complexity: O(1)
-   Best case performance: O(n)
-   Average case performance: O(n*n)
-   Worst case performance: O(n*n)
-   Stable: Yes

### الشرح بالفيديو

[Bubble sort algorithm](https://www.youtube.com/watch?v=Jdtq5uKz-w4)

### Example in JavaScript

```js
let arr = [1, 4, 7, 45, 7,43, 44, 25, 6, 4, 6, 9],
    sorted = false;

while(!sorted) {
  sorted = true;
  for(var i=0; i < arr.length; i++) {
    if(arr[i] < arr[i-1]) {
      let temp = arr[i];
      arr[i] = arr[i-1];
      arr[i-1] = temp;
      sorted = false;
    }
  }
}

```

### Example in Java

```java
public class BubbleSort {
    static void sort(int[] arr) {
        int n = arr.length;
        int temp = 0;
         for(int i=0; i < n; i++){
                 for(int x=1; x < (n-i); x++){
                          if(arr[x-1] > arr[x]){
                                 temp = arr[x-1];
                                 arr[x-1] = arr[x];
                                 arr[x] = temp;
                         }

                 }
         }

    }
    public static void main(String[] args) {

		for(int i=0; i < 15; i++){
			int arr[i] = (int)(Math.random() * 100 + 1);
		}

                System.out.println("array before sorting\n");
                for(int i=0; i < arr.length; i++){
                        System.out.print(arr[i] + " ");
                }
                bubbleSort(arr);
                System.out.println("\n array after sorting\n");
                for(int i=0; i < arr.length; i++){
                        System.out.print(arr[i] + " ");
                }

        }
}

```

### Example in C++

```cpp
// Recursive Implementation
void bubblesort(int arr[], int n)
{
	if(n==1)	//Initial Case
		return;
	bool swap_flag = false;
	for(int i=0;i<n-1;i++)	//After this pass the largest element will move to its desired location.
	{
		if(arr[i]>arr[i+1])
		{
			int temp=arr[i];
			arr[i]=arr[i+1];
			arr[i+1]=temp;
			swap_flag = true;
		}
	}
        // IF no two elements were swapped in the loop, then return, as array is sorted 
	if(swap_flag == false)
		return;
	bubblesort(arr,n-1);	//Recursion for remaining array
}

```

### Example in Swift

```swift
func bubbleSort(_ inputArray: [Int]) -> [Int] {
    guard inputArray.count > 1 else { return inputArray } // make sure our input array has more than 1 element
    var numbers = inputArray // function arguments are constant by default in Swift, so we make a copy
    for i in 0..<(numbers.count - 1) {
        for j in 0..<(numbers.count - i - 1) {
            if numbers[j] > numbers[j + 1] {
                numbers.swapAt(j, j + 1)
            }
        }
    }
    return numbers // return the sorted array
} 

```

### Example in Python

```py
def bubbleSort(arr): 
    n = len(arr) 
    for i in range(n):
        for j in range(0, n-i-1):
                if arr[j] > arr[j+1] : 
                        arr[j], arr[j+1] = arr[j+1], arr[j]
    print(arr)

```

### Example in PHP

```php
function bubble_sort($arr) {
    $size = count($arr)-1;
    for ($i=0; $i<$size; $i++) {
        for ($j=0; $j<$size-$i; $j++) {
            $k = $j+1;
            if ($arr[$k] < $arr[$j]) {
                // Swap elements at indices: $j, $k
                list($arr[$j], $arr[$k]) = array($arr[$k], $arr[$j]);
            }
        }
    }
    return $arr;// return the sorted array
}

$arr = array(1,3,2,8,5,7,4,0);
print("Before sorting");
print_r($arr);

$arr = bubble_sort($arr);
print("After sorting by using bubble sort");
print_r($arr);

```

### Example in C

```c
#include <stdio.h>

int BubbleSort(int array[], int n);

int main(void) {
  int arr[] = {10, 2, 3, 1, 4, 5, 8, 9, 7, 6};
  BubbleSort(arr, 10);

  for (int i = 0; i < 10; i++) {
    printf("%d", arr[i]);
  }
  return 0;
}
int BubbleSort(int array[], n)
{
for (int i = 0 ; i < n - 1; i++)
  {
    for (int j = 0 ; j < n - i - 1; j++)     //n is length of array
    {
      if (array[j] > array[j+1])      // For decreasing order use 
      {
        int swap   = array[j];
        array[j]   = array[j+1];
        array[j+1] = swap;
      }
    }
  }
}

```

## Quick Sort
يعتبر Quick sort خوارزمية ترتيب فعالة من نوع divide and conquer . حيث يملك  Average case time  complexity of O(nlog(n)) و   worst case time complexity being O(n^2)  بناء على اختيار عنصر Pivot الذي يقسم المصفوفة (array) إلى مصفوفتان أصغر (sub arrays).

على سبيل المثال، يعتبر الـ  time complexity للـ  Quick Sort تقريبا `O(nlog(n)) ` عند تقسيم المصفوفة إلى مصفوفتان أصغر متقاربتان في الحجم.

على الجانب الآخر ، عند اختيار Pivot إذا قامت الخوارزمية باختيار Pivot يقوم باستمرار بتقسيم المصفوفة إلى مصفوفتين متباينتين في الحجم يمكن أن يصل Quick sort إلى worst case time complexity of O(n^2).

خطوات عمل Quick sort هي:

* اختيار عنصر ليعمل كـ Pivot ، في حالتنا سنختار آخر عنصر في المصفوفة.
* التقسيم (Partitioning) : ترتيب المصفوفة بحيث تكون كل العناصر الأصغر من الـ Pivot على يساره، وكل العناصر الأكبر منه على يمينه.
* اعادة تنفيذ Quicksort recursively، مع الأخذ بالاعتبار أن الـ Pivot السابق قام بطريقة صحيحة بتقسيم المصفوفة الى قسمين على اليمين وعلى اليسار (يمكن العثور على توضيح أكثر تفصيلا في الcomments بالأسفل). 

## أمثلة تطبيقية باستخدام عدة لغات بالأسفل:

### Implementation in JavaScript:

```js
const arr = [6, 2, 5, 3, 8, 7, 1, 4];

const quickSort = (arr, start, end) => {

  if(start < end) {

    // You can learn about how the pivot value is derived in the comments below
    let pivot = partition(arr, start, end);

    // Make sure to read the below comments to understand why pivot - 1 and pivot + 1 are used
    // These are the recursive calls to quickSort
    quickSort(arr, start, pivot - 1);
    quickSort(arr, pivot + 1, end);
  } 

}

const partition = (arr, start, end) => { 
  let pivot = end;
  // Set i to start - 1 so that it can access the first index in the event that the value at arr[0] is greater than arr[pivot]
  // Succeeding comments will expound upon the above comment
  let i = start - 1,
      j = start;

  // Increment j up to the index preceding the pivot
  while (j < pivot) {

    // If the value is greater than the pivot increment j
    if (arr[j] > arr[pivot]) {
      j++;
    }

    // When the value at arr[j] is less than the pivot:
    // increment i (arr[i] will be a value greater than arr[pivot]) and swap the value at arr[i] and arr[j]
    else {
      i++;
      swap(arr, j, i);
      j++;
    }

  }

  //The value at arr[i + 1] will be greater than the value of arr[pivot]
  swap(arr, i + 1, pivot);

  //You return i + 1, as the values to the left of it are less than arr[i+1], and values to the right are greater than arr[i + 1]
  // As such, when the recursive quicksorts are called, the new sub arrays will not include this the previously used pivot value
  return i + 1;
}

const swap = (arr, firstIndex, secondIndex) => {
  let temp = arr[firstIndex];
  arr[firstIndex] = arr[secondIndex];
  arr[secondIndex] = temp;
}

quickSort(arr, 0, arr.length - 1);
console.log(arr);

```

### Implementation in C

```c
#include<stdio.h>  
void swap(int* a, int* b) 
{ 
    int t = *a; 
    *a = *b; 
    *b = t; 
}
int partition (int arr[], int low, int high) 
{ 
    int pivot = arr[high];     
    int i = (low - 1);  
  
    for (int j = low; j <= high- 1; j++) 
    { 
        if (arr[j] <= pivot) 
        { 
            i++;    
            swap(&arr[i], &arr[j]); 
        } 
    } 
    swap(&arr[i + 1], &arr[high]); 
    return (i + 1); 
}
void quickSort(int arr[], int low, int high) 
{ 
    if (low < high) 
    {
        int pi = partition(arr, low, high); 
  
        quickSort(arr, low, pi - 1); 
        quickSort(arr, pi + 1, high); 
    } 
} 
  

void printArray(int arr[], int size) 
{ 
    int i; 
    for (i=0; i < size; i++) 
        printf("%d ", arr[i]); 
    printf("n"); 
} 
  

int main() 
{ 
    int arr[] = {10, 7, 8, 9, 1, 5}; 
    int n = sizeof(arr)/sizeof(arr[0]); 
    quickSort(arr, 0, n-1); 
    printf("Sorted array: n"); 
    printArray(arr, n); 
    return 0; 
} 

```

### Implementation in Python3

```
import random

z=[random.randint(0,100) for i in range(0,20)]

def quicksort(z):
    if(len(z)>1):        
        piv=int(len(z)/2)
        val=z[piv]
        lft=[i for i in z if i<val]
        mid=[i for i in z if i==val]
        rgt=[i for i in z if i>val]

        res=quicksort(lft)+mid+quicksort(rgt)
        return res
    else:
        return z
        
ans1=quicksort(z)
print(ans1)

```

### Implementation in MATLAB

```
a = [9,4,7,3,8,5,1,6,2];

sorted = quicksort(a,1,length(a));

function [unsorted] =  quicksort(unsorted, low, high)
    if low < high
        [pInd, unsorted] = partition(unsorted, low, high);
        unsorted = quicksort(unsorted, low, pInd-1);
        unsorted = quicksort(unsorted, pInd+1, high);
    end

end

function [pInd, unsorted] = partition(unsorted, low, high)
    i = low-1;
    for j = low:1:high-1
        if unsorted(j) <= unsorted(high)
            i = i+1;
            unsorted([i,j]) = unsorted([j,i]);
            
        end
    end
    unsorted([i+1,high]) = unsorted([high,i+1]);
    pInd = i+1;

end

```
الـ Space complexity لـ Quick sort هي  `O(n)`. وهذا يعتبر تحسن عن معظم خوارزميات divide and conquer والتي تحتاج عاظة إلى  `O(nlong(n))`  space.

يحقق quick sort هذا عن طريق تغيير ترتيب العناصر داخل المصفوفة. مقارنة بـ   [merge sort](https://guide.freecodecamp.org/algorithms/sorting-algorithms/merge-sort) الذي يقوم بإنشاء مصفوفتين جديدتين، كل منهما بحجم   `n/2` في كل استدعاء (function call).

مع ذلك نظل لم نتخلص من مشكلة ترتيب العناصر في وقت `O(n*n)` ولكن هذا يمكن حله عن طريق استخدام  random pivot  

### Complexity

Best, average, worst, memory:  n log(n)n log(n)n 2log(n). It's not a stable algorithm, and quicksort is usually done in-place with O(log(n)) stack space.

الـ Space complexity لـ Quick sort هي  `O(n)`. وهذا يعتبر تحسن عن معظم خوارزميات divide and conquer والتي تحتاج عاظة إلى  `O(nlong(n))`  space.

## Timsort

Timsort هو خوارزمية ترتيب سريعة تعمل كـ stable O(N log(N)) complexity.

Timesort هو مزيج بين Insertion sort و Mergesort. حيث يتم ترتيب الأجزاء الصغيرة باستعمال Insertion Sort ولاحقا يتم دمجها معا باستخدام Mergesort. 

This algorithm is implemented in Java’s Arrays.sort() as well as Python’s sorted() and sort(). 

A quick implementation in Python:

```py
def binary_search(the_array, item, start, end):
    if start == end:
        if the_array[start] > item:
            return start
        else:
            return start + 1
    if start > end:
        return start

    mid = round((start + end)/ 2)

    if the_array[mid] < item:
        return binary_search(the_array, item, mid + 1, end)

    elif the_array[mid] > item:
        return binary_search(the_array, item, start, mid - 1)

    else:
        return mid

"""
Insertion sort that timsort uses if the array size is small or if
the size of the "run" is small
"""
def insertion_sort(the_array):
    l = len(the_array)
    for index in range(1, l):
        value = the_array[index]
        pos = binary_search(the_array, value, 0, index - 1)
        the_array = the_array[:pos] + [value] + the_array[pos:index] + the_array[index+1:]
    return the_array

def merge(left, right):
    """Takes two sorted lists and returns a single sorted list by comparing the
    elements one at a time.
    [1, 2, 3, 4, 5, 6]
    """
    if not left:
        return right
    if not right:
        return left
    if left[0] < right[0]:
        return [left[0]] + merge(left[1:], right)
    return [right[0]] + merge(left, right[1:])

def timsort(the_array):
    runs, sorted_runs = [], []
    length = len(the_array)
    new_run = [the_array[0]]

    # for every i in the range of 1 to length of array
    for i in range(1, length):
        # if i is at the end of the list
        if i == length - 1:
            new_run.append(the_array[i])
            runs.append(new_run)
            break
        # if the i'th element of the array is less than the one before it
        if the_array[i] < the_array[i-1]:
            # if new_run is set to None (NULL)
            if not new_run:
                runs.append([the_array[i]])
                new_run.append(the_array[i])
            else:
                runs.append(new_run)
                new_run = []
        # else if its equal to or more than
        else:
            new_run.append(the_array[i])

    # for every item in runs, append it using insertion sort
    for item in runs:
        sorted_runs.append(insertion_sort(item))
    
    # for every run in sorted_runs, merge them
    sorted_array = []
    for run in sorted_runs:
        sorted_array = merge(sorted_array, run)

    print(sorted_array)

timsort([2, 3, 1, 5, 6, 7])

```

### Complexity:

Tim sort has a stable Complexity of O(N log(N)) ويمكن مقارنته بـ Quicksort ويمكنك إيجاد مقارنة مفصلة بينهم هنا:  [chart](https://cdn-images-1.medium.com/max/1600/1*1CkG3c4mZGswDShAV9eHbQ.png).

## Merge Sort
Merge Sort  هو خوارزمية من نوع  [Divide and Conquer](https://guide.freecodecamp.org/algorithms/divide-and-conquer-algorithms). حيث يقوم بتقسيم المصفوفة إلى نصفين، ثم اعادة العملية مرة اخرى على كل من النصفين ثم إعادة دمجهم مرة اخرى بعد ترتيبهم. الجزء الرئيسي في الخوارزمية هو الجزء الخاص بدمج المصفوفتين المرتبتين في مصفوفة واحدة مرتبة. يمكن تلخيص عملية ترتيب مصفوفة تتكون من N من الأرقام الصحيحة (Integers) في ثلاث خطوات:
* تقسيم المصفوفة (array) الى نصفين.
* ترتيب النصفين الأيمن والأيسر بنفس الطريقة (recurring algorithm).
* دمج النصفين المرتبين.

هناك شئ يسمى بـ  [Two Finger Algorithm](https://en.wikipedia.org/wiki/Cheney%27s_algorithm)  وهو الذي يعمل على دمج المصفوفتان المرتبتان معا. باستخدام هذا الـ  subroutine و استدعاء merge sort function مع النصفين بشكل recursively نحصل على المصفوفة النهائية المرتبة التي نبحث عنها.

بما أن هذه الخوارزمية هي recursion based algorithm سنناقش الـ recurrence relation الخاص بها. الـ  recurrence relation ببساطة هو طريقة بسيطة لتمثيل مشكلة معقدة اعتمادا على تقسيمها لعدة مشاكل أبسط (subproblems).

`T(n) = 2 * T(n / 2) + O(n)`

إذا أردنا التعبير عنها باللغةالعربية، فهي ببساطة أننا نقوم بتقسيم المشكلة الى جزئين اصغر في كل خطوة و بعد ذلك نستطيع اعدة دمجهم مرة اخرى في نهاية كل خطوة مع  linear amount of work. 

### Complexity
الميزة الأكبر من استخدام Merge Sort هي أن الـ [time complexity](https://www.youtube.com/watch?v=V42FBiohc6c&list=PL2_aWCzGMAwI9HK8YPVBjElbLbI3ufctn) الخاص بها هو فقط n*log(n) لترتيب المصفوفة بالكامل. وهو أفضل كثيرا من  n^2 running time مع Bubble Sort أو Insertion Sort.

قبل كتابة الكود دعنا نفهم أولا كيف يعمل Merge Sort بمساعدة هذا المخطط.
![](https://www.freecodecamp.org/news/content/images/2021/06/4712ef1a5d856dbb4af393fcc08a820a38787395.png)

-   في البداية نملك مصفوفة مكونة من 6 عناصر غير مرتبة Arr(5, 8, 3, 9, 1, 2)
-   ثم نقوم بتقسيمها إلى نصفين Arr1 = (5, 8, 3) و Arr2 = (9, 1, 2).
-   مرة اخرى نقسم كل array الى نصفين : Arr3 = (5, 8) و Arr4 = (3) و Arr5 = (9, 1) و Arr6 = (2)
-   مرة اخرى نقوم بتقسيمها الى نصفين : Arr7 = (5), Arr8 = (8), Arr9 = (9), Arr10 = (1) و Arr6 = (2)
-   الآن نقوم بمقارنة المصفوفات الجديدة معا لدمجهم مرة اخرى بطريقة مرتبة.

### الخصائص:

-   Space Complexity: O(n)
-   Time Complexity: O(n*log(n)). The time complexity for the Merge Sort يمكن أن تكون غير واضحة من أول نظرة . The log(n) factor تم التعرف عليه من خلال ال recurrence relation المذكور بالأعلى.
-   Sorting In Place: No in a typical implementation
-   Stable: Yes
-   Parallelizable :yes (Several parallel variants are discussed in the third edition of Cormen, Leiserson, Rivest, and Stein's Introduction to Algorithms.)

### **C++ Implementation**

```cpp
void merge(int array[], int left, int mid, int right)
{
    int i, j, k;

    // Size of left sublist
int size_left = mid - left + 1;

// Size of right sublist
int size_right =  right - mid;

/* create temp arrays */
int Left[size_left], Right[size_right];

/* Copy data to temp arrays L[] and R[] */
for(i = 0; i < size_left; i++)
{
    Left[i] = array[left+i];
}

for(j = 0; j < size_right; j++)
{
    Right[j] = array[mid+1+j];
}

// Merge the temp arrays back into arr[left..right]
i = 0; // Initial index of left subarray
j = 0; // Initial index of right subarray
k = left; // Initial index of merged subarray

while (i < size_left && j < size_right)
{
    if (Left[i] <= Right[j])
    {
        array[k] = Left[i];
        i++;
    }
    else
    {
        array[k] = Right[j];
        j++;
    }
    k++;
}

// Copy the remaining elements of Left[]
while (i < size_left)
{
    array[k] = Left[i];
    i++;
    k++;
}

// Copy the rest elements of R[]
while (j < size_right)
{
    array[k] = Right[j];
    j++;
    k++;
}
}

void mergeSort(int array[], int left, int right)
{
    if(left < right)
    {
        int mid = (left+right)/2;

        // Sort first and second halves
    mergeSort(array, left, mid);
    mergeSort(array, mid+1, right);

    // Finally merge them
    merge(array, left, mid, right);
}
}
```

### **JavaScript Implementation**

```js
function mergeSort (arr) {
  if (arr.length < 2) return arr;
  var mid = Math.floor(arr.length /2);
  var subLeft = mergeSort(arr.slice(0,mid));
  var subRight = mergeSort(arr.slice(mid));
  return merge(subLeft, subRight);
}
```
أولا نفحص طول المصفوفة (array length). إذا ساوت قيمته 1 فإننا ببساطه نعود  return the array. يمكن اعتبار هذه الحالة هي الـ  base case الخاصة بنا. إذا لم تساوي 1، نحدد منتصف المصفوفة ونقوم بتقسيمها إلى نصفين. بعد ذلك نقوم بترتيب النصفين بنفس الطريقة عن طريق recursive calls to MergeSort function. 

```js
function merge (a,b) {
    var result = [];
    while (a.length >0 && b.length >0)
        result.push(a[0] < b[0]? a.shift() : b.shift());
    return result.concat(a.length? a : b);
}
```
عند دمج النصفين، نقوم بتخزين الناتج فيauxilliary array. حيث نقوم بمقارنة العنصر الأول في المصفوفة الأولى مع العنصر الأول في المصفوفة الثانية. العنصر الأصغر بينهما يتم نقله إلى الناتج النهائي (results array) وحذفه من الـ respective arrays باستخدام  shift() operator. في حال تبقي عناصر في أحد المصفوفتين، نقوم ببساطة بدمجها في نهاية results array. وهذا هو الناتج النهائي: 


```js
var test = [5,6,7,3,1,3,15];
console.log(mergeSort(test));

>> [1, 3, 3, 5, 6, 7, 15]
```

### الشرح بالفيديو على يوتيوب:

Here's a good YouTube video that  [walks through the topic in detail](https://www.youtube.com/watch?v=TzeBrDU-JaY).

### Implementaion in JS

```js
const list = [23, 4, 42, 15, 16, 8, 3]

const mergeSort = (list) =>{
  if(list.length <= 1) return list;
  const middle = list.length / 2 ;
  const left = list.slice(0, middle);
  const right = list.slice(middle, list.length);
  return merge(mergeSort(left), mergeSort(right));
}

const merge = (left, right) => {
  var result = [];
  while(left.length || right.length) {
    if(left.length && right.length) {
      if(left[0] < right[0]) {
        result.push(left.shift())
      } else {
        result.push(right.shift())
      }
    } else if(left.length) {
        result.push(left.shift())
      } else {
        result.push(right.shift())
      }
    }
  return result;
}

console.log(mergeSort(list)) // [ 3, 4, 8, 15, 16, 23, 42 ]

```

### Implementation in C

```c
#include<stdlib.h> 
#include<stdio.h>
void merge(int arr[], int l, int m, int r) 
{ 
    int i, j, k; 
    int n1 = m - l + 1; 
    int n2 =  r - m; 
  
    
    int L[n1], R[n2]; 
  
    for (i = 0; i < n1; i++) 
        L[i] = arr[l + i]; 
    for (j = 0; j < n2; j++) 
        R[j] = arr[m + 1+ j];
    i = 0; 
    j = 0; 
    k = l; 
    while (i < n1 && j < n2) 
    { 
        if (L[i] <= R[j]) 
        { 
            arr[k] = L[i]; 
            i++; 
        } 
        else
        { 
            arr[k] = R[j]; 
            j++; 
        } 
        k++; 
    } 
  
    
    while (i < n1) 
    { 
        arr[k] = L[i]; 
        i++; 
        k++; 
    } 
  
    while (j < n2) 
    { 
        arr[k] = R[j]; 
        j++; 
        k++; 
    } 
} 
  
void mergeSort(int arr[], int l, int r) 
{ 
    if (l < r) 
    {  
        int m = l+(r-l)/2; 
  
        
        mergeSort(arr, l, m); 
        mergeSort(arr, m+1, r); 
  
        merge(arr, l, m, r); 
    } 
}
void printArray(int A[], int size) 
{ 
    int i; 
    for (i=0; i < size; i++) 
        printf("%d ", A[i]); 
    printf("\n"); 
} 
int main() 
{ 
    int arr[] = {12, 11, 13, 5, 6, 7}; 
    int arr_size = sizeof(arr)/sizeof(arr[0]); 
  
    printf("Given array is \n"); 
    printArray(arr, arr_size); 
  
    mergeSort(arr, 0, arr_size - 1); 
  
    printf("\nSorted array is \n"); 
    printArray(arr, arr_size); 
    return 0; 

```

### Implementation in C++

لنعتبر أن لدينا array A = {2,5,7,8,9,12,13} و نحتاج لـ array C  مرتبة تصاعديا

```cpp
void mergesort(int A[],int size_a,int B[],int size_b,int C[])
{
     int token_a,token_b,token_c;
     for(token_a=0, token_b=0, token_c=0; token_a<size_a && token_b<size_b; )
     {
          if(A[token_a]<=B[token_b])
               C[token_c++]=A[token_a++];
          else
               C[token_c++]=B[token_b++];
      }
      
      if(token_a<size_a)
      {
          while(token_a<size_a)
               C[token_c++]=A[token_a++];
      }
      else
      {
          while(token_b<size_b)
               C[token_c++]=B[token_b++];
      }

}

```

### Implementation in Python

```py
def merge(left,right,compare):
	result = [] 
	i,j = 0,0
	while (i < len(left) and j < len(right)):
		if compare(left[i],right[j]):
			result.append(left[i])
			i += 1
		else:
			result.append(right[j])
			j += 1
	while (i < len(left)):
		result.append(left[i])
		i += 1
	while (j < len(right)):
		result.append(right[j])
		j += 1
	return result

def merge_sort(arr, compare = lambda x, y: x < y):
     #Used lambda function to sort array in both(increasing and decresing) order.
     #By default it sorts array in increasing order
	if len(arr) < 2:
		return arr[:]
	else:
		middle = len(arr) // 2
		left = merge_sort(arr[:middle], compare)
		right = merge_sort(arr[middle:], compare)
		return merge(left, right, compare) 

arr = [2,1,4,5,3]
print(merge_sort(arr))

```

### Implementation in Java

```java
public class mergesort {

	public static int[] mergesort(int[] arr,int lo,int hi) {
		
		if(lo==hi) {
			int[] ba=new int[1];
			ba[0]=arr[lo];
			return ba;
		}
		
		int mid=(lo+hi)/2;
		int arr1[]=mergesort(arr,lo,mid);
		int arr2[]=mergesort(arr,mid+1,hi);
		return merge(arr1,arr2);
	}
	
	public static int[] merge(int[] arr1,int[] arr2) {
		int i=0,j=0,k=0;
		int n=arr1.length;
		int m=arr2.length;
		int[] arr3=new int[m+n];
		while(i<n && j<m) {
			if(arr1[i]<arr2[j]) {
				arr3[k]=arr1[i];
				i++;
			}
			else {
				arr3[k]=arr2[j];
				j++;
			}
			k++;
		}
		
		while(i<n) {
			arr3[k]=arr1[i];
			i++;
			k++;
		}
		
		while(j<m) {
			arr3[k]=arr2[j];
			j++;
			k++;
		}
		
		return arr3;
		
	}
	
	public static void main(String[] args) {
		// TODO Auto-generated method stub
		int arr[]= {2,9,8,3,6,4,10,7};
		int[] so=mergesort(arr,0,arr.length-1);
		for(int i=0;i<arr.length;i++)
			System.out.print(so[i]+" ");
	}

}

```

### Example in Java

```java
public class mergesort {
  public static int[] mergesort(int[] arr, int lo, int hi) {
    if (lo == hi) {
      int[] ba = new int[1];
      ba[0] = arr[lo];
      return ba;
    }
    int mid = (lo + hi) / 2;
    int arr1[] = mergesort(arr, lo, mid);
    int arr2[] = mergesort(arr, mid + 1, hi);
    return merge(arr1, arr2);
  }

  public static int[] merge(int[] arr1, int[] arr2) {
    int i = 0, j = 0, k = 0;
    int n = arr1.length;
    int m = arr2.length;
    int[] arr3 = new int[m + n];
    while (i < n && j < m) {
      if (arr1[i] < arr2[j]) {
        arr3[k] = arr1[i];
        i++;
      } else {
        arr3[k] = arr2[j];
        j++;
      }
      k++;
    }
    while (i < n) {
      arr3[k] = arr1[i];
      i++;
      k++;
    }
    while (j < m) {
      arr3[k] = arr2[j];
      j++;
      k++;
    }
    return arr3;
  }

  public static void main(String[] args) {
    int arr[] = {2, 9, 8, 3, 6, 4, 10, 7};
    int[] so = mergesort(arr, 0, arr.length - 1);
    for (int i = 0; i < arr.length; i++)
      System.out.print(so[i] + " ");
  }
}

```