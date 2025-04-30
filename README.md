# BrutalMemory

**BrutalMemory** is a powerful C# memory editing library that allows reading, writing, and scanning memory of external processes. It is designed with flexibility and extensibility in mind, useful for building tools such as game trainers, cheat loaders, or debugging utilities.

> 🛡️ This project is intended for **educational and ethical use only**. Do **not** use it to violate terms of service or local laws.

---

## 🚀 Features

- 🧠 Attach to processes by name.
- 🔍 Perform AoB (Array of Bytes) pattern scanning with wildcards.
- 📝 Read and write memory with support for multiple data types.
- 📌 Replace byte patterns in memory (e.g., patch instructions).
- 🔄 Suspend and resume remote process threads.
- 🔒 Verify memory regions for safe access.

---

## 📦 Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/BrutalMemory.git
    ```

2. Add the `Memory.cs` file to your C# project.

3. Build the project using Visual Studio or `dotnet build`.

> ✅ Compatible with .NET 6/7/8. Administrator privileges may be required for some operations.

---

## 🧠 Basic Usage

### 1. Attach to a Process

```csharp
var mem = new BrutalMemory.Memory();
bool success = mem.SetProcess(new[] { "HD-Player" });

if (!success)
{
    Console.WriteLine("Failed to attach to process.");
    return;
}
