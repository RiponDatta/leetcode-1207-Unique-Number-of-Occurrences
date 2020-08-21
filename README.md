# leetcode 1207- Unique Number of Occurrences

## Java
```Java
```

## C#
```C#
public static bool UniqueOccurrences(int[] arr)
{
    var frequency = new Dictionary<int, int>();
    for (int i = 0; i < arr.Length; i++)
    {
        if (frequency.ContainsKey(arr[i]))
            frequency[arr[i]]++;
        else
            frequency.Add(arr[i], 1);
    }
    var freqOccurrences = new Hashtable();
    foreach (var x in frequency)
    {
        if (!freqOccurrences.Contains(x.Value))
            freqOccurrences.Add(x.Value, 1);
        else return false;
    }
    return true;
}
```
