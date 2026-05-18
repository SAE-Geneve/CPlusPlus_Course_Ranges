# C++ Ranges — Companion Examples

Runnable code for every chapter of the **C++ Ranges** lecture
([`cpp_ranges_lecture.md`](https://github.com/StudioAlbert/Knowledges/blob/main/C%2B%2B%20Advanced/cpp_ranges_lecture.md)). Each folder is a
self-contained, compilable program; the folder name matches the slide
title.

## About

Companion code for **C++ Ranges — A modern STL, in 3 hours**
([lecture deck](https://github.com/StudioAlbert/Knowledges/blob/main/C%2B%2B%20Advanced/cpp_ranges_lecture.md)). The course covers:

- **Why Ranges?** — the STL boilerplate/safety tax; what a range is
- **Range Algorithms** — `std::ranges::` algorithms and projections
- **Views & Pipelines** — lazy evaluation, `|` composition, the role of `auto`
- **Lifetimes & Patterns** — owning vs. borrowing views
- **The Range Hierarchy** — the five range-concept tiers
- **C++23 & Beyond** — `std::ranges::to`, `enumerate` / `zip` / `slide`
- **Exercises** — two guided STL→ranges refactors, with solutions

Each chapter maps to a runnable folder (see the table below).

## Requirements

- A **C++23** toolchain. Examples 09–10 and both exercises use
  `std::ranges::to`, `std::views::enumerate` / `zip` / `slide`, and
  `std::ranges::fold_left`.
  - GCC **14+**, Clang **18+**, or MSVC **19.38+** (VS 2022 17.8+).
- CMake **3.20+**.

## Build & run — CLion

Open this folder in CLion. It detects the top-level `CMakeLists.txt`
and exposes one run target per chapter. Pick a target and press Run.

Each subfolder is *also* a standalone CMake project, so you can open an
individual chapter folder directly if you prefer.

## Build & run — command line

```sh
cmake -S . -B build
cmake --build build
./build/examples/01_the_iterator_problem/01_the_iterator_problem
```

(On Windows the binary is under `build\examples\...\Debug\*.exe` with
the Visual Studio generator.)

## Layout

| # | Folder | Lecture slide |
|---|--------|---------------|
| 01 | `examples/01_the_iterator_problem` | The Iterator Problem |
| 02 | `examples/02_range_concept_basics` | Range Concept Basics |
| 03 | `examples/03_range_algorithms_basics` | Range Algorithms Basics |
| 04 | `examples/04_composing_pipelines` | Composing Pipelines with `\|` |
| 05 | `examples/05_projections_and_constraints` | Projections & Constraints |
| 06 | `examples/06_views_lazy_evaluation` | Views & Lazy Evaluation |
| 07 | `examples/07_owning_views` | Owning Views |
| 08 | `examples/08_borrowing_views` | Borrowing Views |
| 09 | `examples/09_ranges_to` | `std::ranges::to` |
| 10 | `examples/10_cpp23_enumerate_zip_chunk` | enumerate / zip / chunk / slide |
| — | `exercises/01_refactor_classic_loop` | Exercise 1 (solution) |
| — | `exercises/02_top3_followers` | Exercise 2 (solution) |
