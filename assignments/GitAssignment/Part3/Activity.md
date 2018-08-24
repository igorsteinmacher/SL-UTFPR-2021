# Activity 7, Part 3: Lexical Conflicts

## Model 1: Orientation

```
$ git branch
  feature-bar
* master
```

1. What branch is the user on?

    ```

    ```


## Model 2: Merge Attempt

```
11:54 $ git merge feature-bar
Auto-merging A.java
CONFLICT (content): Merge conflict in A.java
Automatic merge failed; fix conflicts and then commit the result.
```

1. What branch is being merged?

    ```


    ```

2. What branch is being merged **into**?

    ```


    ```

3. What file has a conflict?

    ```


    ```

4. What are we supposed to do now?

    ```


    ```

## Model 3: Conflicted Status

```
$ git status
On branch master
You have unmerged paths.
  (fix conflicts and run "git commit")
  (use "git merge --abort" to abort the merge)

Changes to be committed:

	modified:   B.java

Unmerged paths:
  (use "git add <file>..." to mark resolution)

	both modified:   A.java
```

1. Does B.java have conflicts? What tells you that?

    ```


    ```

2. Does A.java have conflicts? What tells you that?

    ```


    ```

3. Is the merge complete? What tells you that?

    ```


    ```

4. If you want to give up on the merge, what do you do?

    ```

    ```

5. What do you need to do to resolve the conflict and complete the merge?

    ```

    ```

## Model 4: A Conflict

Below is the contents of A.java

```
public class A {

	public void foo() {
<<<<<<< HEAD
		B b = new B();
		b.bar();
=======
		System.out.println("Hi");
>>>>>>> feature-bar
	}

}
```

1. What conflicted code comes from the `master` branch (remember it's the branch we are merging **into**)?

    ```


    ```

2. What conflicted code comes from the `feature-bar` branch?

    ```


    ```

3. Give one resolution of the conflict.

    ```







    ```

4. Assuming you make the above changes and save the file, what commands do you issue to finish the merge?

    ```



    ```
