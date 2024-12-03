# Executor Framework in Java

The **Executor Framework** is a part of Java's **concurrency package (`java.util.concurrent`)**, introduced in Java 5. It simplifies multithreaded programming by decoupling task submission from the mechanics of how tasks are executed.

---

## Key Components

| **Component**                  | **Description**                                                                                                     |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------|
| **Executor**                   | The base interface in the framework. It has a single method: `void execute(Runnable command)`.                      |
| **ExecutorService**            | Subinterface of `Executor` with additional features like task lifecycle management and returning results.           |
| **ScheduledExecutorService**   | Extends `ExecutorService` to support scheduling tasks to run at fixed rates or delays.                              |
| **ThreadPoolExecutor**         | A concrete implementation of `ExecutorService` that executes tasks using a configurable thread pool.               |
| **ForkJoinPool**               | A pool designed for parallelism, breaking tasks into subtasks recursively and joining results.                     |

---

## Important Classes

| **Class**                      | **Description**                                                                                                     |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------|
| **Executors**                  | Utility class for creating and managing pre-configured thread pools like `newFixedThreadPool()`.                     |
| **Future**                     | Represents the result of an asynchronous computation.                                                               |
| **Callable**                   | Similar to `Runnable`, but can return a result and throw checked exceptions.                                        |
| **CompletionService**          | Combines task submission and result retrieval efficiently.                                                          |

---

## Predefined Thread Pool Types

| **Thread Pool Type**               | **Method**                               | **Description**                                                                                     |
|------------------------------------|------------------------------------------|-----------------------------------------------------------------------------------------------------|
| **Fixed Thread Pool**              | `Executors.newFixedThreadPool(n)`        | Pool with a fixed number of threads. Excess tasks wait in a queue until threads are free.          |
| **Cached Thread Pool**             | `Executors.newCachedThreadPool()`        | Dynamic thread pool that creates new threads as needed but reuses idle threads.                    |
| **Single Thread Executor**         | `Executors.newSingleThreadExecutor()`    | Executes tasks sequentially with a single thread.                                                  |
| **Scheduled Thread Pool**          | `Executors.newScheduledThreadPool(n)`    | Allows scheduling tasks to run after a delay or periodically.                                      |
| **Work Stealing Pool**             | `Executors.newWorkStealingPool()`        | Introduced in Java 8, creates threads that steal tasks from other threads' queues for better usage.|

---

## Common Methods in `ExecutorService`

| **Method**                           | **Description**                                                                                                     |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| `void execute(Runnable command)`     | Executes a `Runnable` task asynchronously.                                                                          |
| `Future<?> submit(Runnable task)`    | Submits a `Runnable` task and returns a `Future` representing the task's result.                                    |
| `<T> Future<T> submit(Callable<T>)`  | Submits a `Callable` task and returns a `Future` for the result.                                                    |
| `void shutdown()`                    | Initiates an orderly shutdown, stopping acceptance of new tasks.                                                   |
| `List<Runnable> shutdownNow()`       | Attempts to stop all running tasks immediately and returns a list of pending tasks.                                 |
| `boolean isShutdown()`               | Checks if the ExecutorService is shut down.                                                                         |
| `boolean isTerminated()`             | Checks if all tasks are completed after shutdown.                                                                   |
| `List<Future<T>> invokeAll(...)`     | Executes a collection of tasks and waits for all to complete, returning results as a list of `Future` objects.      |
| `<T> T invokeAny(...)`               | Executes a collection of tasks and returns the result of the first successfully completed task.                     |

---

## Code Examples

### Example 1: Using `ExecutorService` with `FixedThreadPool`

```java
import java.util.concurrent.ExecutorService;
import java.util.concurrent.Executors;

public class ExecutorExample {
    public static void main(String[] args) {
        ExecutorService executor = Executors.newFixedThreadPool(3); // Pool of 3 threads.

        for (int i = 1; i <= 5; i++) {
            int taskNumber = i;
            executor.execute(() -> {
                System.out.println("Task " + taskNumber + " executed by " + Thread.currentThread().getName());
            });
        }

        executor.shutdown(); // Shut down the executor
    }
}
