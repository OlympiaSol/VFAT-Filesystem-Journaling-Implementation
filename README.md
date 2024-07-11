## VFAT Filesystem Journaling Implementation

### Overview

This project was part of the MYY601 Operating Systems course at the University of Ioannina. The primary objective was to extend the VFAT filesystem within the Linux Kernel Library (LKL) to support journaling. Journaling records modifications to the filesystem, allowing for efficient recovery in case of crashes.

### Project Description

#### Linux Kernel Library (LKL)

LKL is a user-space implementation of the Linux kernel, enabling reuse of kernel code in applications with minimal changes. LKL runs within a user process, simplifying kernel functionalities by eliminating the need for multi-process support and user-kernel protection.

#### VFAT Filesystem

VFAT is an extended version of the FAT filesystem, supporting long filenames up to 255 characters. The VFAT filesystem is commonly used in removable storage media. The project involved implementing a simple journaling mechanism to record filesystem modifications.

### Getting Started

#### Prerequisites

- **C Programming Language**: The implementation was done in C.
- **Pthreads Library**: Used for thread management and synchronization.
- **Virtual Machine**: Downloaded and set up the provided virtual machine running Debian Linux 64-bit.


#### Running the Test Applications

1. Created and mounted a VFAT disk image:
   ```sh
   ./disk.sh -t vfat
   ```
2. Executed various test operations:
   ```sh
   ./cptofs -i /tmp/disk -t vfat lklfuse.o /
   ./disk -t vfat -d /tmp/disk
   ```

### Implementation Steps

1. **Understanding VFAT Operations**: Investigated VFAT filesystem operations and their interactions with LKL.
2. **Basic Journaling**: Implemented a basic journaling mechanism to log important operations and their parameters.
3. **Enhanced Journaling**: Extended the logging to include more detailed information and ensured synchronization using Pthreads.

### Deliverables

- **Source Code**: Submitted only the modified files in a zip archive `lkl-source.zip`.
- **Report**: Detailed report (`Report.pdf`) including:
  - Names and registration numbers of the group members.
  - Description of the implemented functionalities.
  - Detailed explanation of each code modification.
  - Performance test results and analysis.
  - Output of the `make` command and execution results.


### Additional Resources

- [LKL Documentation](https://www.cse.uoi.gr/~stergios/teaching/myy601/lab/lkl-dox/html/index.html)

For more details, feel free to take a look at my report PDF file. Here is a brief summary of what the PDF contains:

- **Introduction**: Overview of the project objectives and requirements.
- **Setup Instructions**: Steps to set up the virtual machine and necessary software.
- **Implementation Details**: Detailed explanation of the journaling implementation, including synchronization techniques and code modifications.
- **Performance Evaluation**: Results of performance tests under different scenarios and analysis of the outcomes.
- **Conclusion**: Summary of the project's achievements and potential areas for improvement.

You can find the full report in the attached `Report.pdf` file.

---

## Useful Links

- Documentation: https://docs.askthecode.ai
- GitHub: https://github.com/askthecode/documentation
- Twitter: https://twitter.com/askthecode_ai

---
