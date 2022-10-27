** Algorithm for the problem.

Here trie is used to solve this problem efficiently.

> Step 1. Build the trie by reading every word one by one from the selected file.
>  Step 2. While building the trie also build a dequeue which contains `<word,suffix>` pairs if any w.r.t the previously existing valid words in the trie. 
> Step 3. Initialize the `longest`, `second_longest`, and `max_length` variables.
> Step 4. Repeat untill the queue is empty, POP the `<word,suffix>` pairs from the dequeue.
> > i) Check if the suffix of the word contains any valid word i.e. `prefix` from the trie and if `length (word) > max_length` , set 
> `second_longest = longest` , 
> `longest = word` and 
> `max_length = length(word)`.
> >ii) Else get all the prefixes of the current suffix of the word , and find the new suffixes w.r.t each and every prefix length. Append the new `<word,suffix>` pairs into the deque. 
> Step 5. Return the longest and second_longest words

** Procedure to execute the program.
>Open the Solution.py file and scroll to the code segment with the comment #Change the file path here.
>Enter the relative path of the text file for the input w.r.t the solution file as a parameter to sol.buildTrie().
>Execute the file Solution.py.
