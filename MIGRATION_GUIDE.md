# Swing to JavaFX Migration Guide

This project serves as a personal study and documentation effort on migrating legacy Java Swing applications to JavaFX.  
It complements my fork of [JetUML](https://github.com/prmr/JetUML), which transitioned from Swing to JavaFX starting in version 2.0.

---

## 🎯 Goals
- Understand practical steps for modernizing Swing-based desktop applications.
- Explore incremental migration techniques (Swing + JavaFX hybrid).
- Document challenges, solutions, and patterns observed during study.
- Experiment with small UI components as test cases.

---

## 🛠 Migration Plan Template

### 1️⃣ Inventory existing UI
- List main windows, dialogs, panels.
- Identify custom-painted components or graphics-heavy areas.

### 2️⃣ Choose a migration approach
- Hybrid: integrate JavaFX into Swing via `JFXPanel`, or embed Swing in JavaFX via `SwingNode`.
- Full refactor: rewrite components fully in JavaFX.

### 3️⃣ Set up JavaFX scaffolding
- Add OpenJFX as a dependency (modular or classpath).
- Create `Application` subclass with `Stage` and `Scene`.

### 4️⃣ Incremental migration
- Replace non-critical dialogs and panels first.
- Migrate custom painting to JavaFX `Canvas` or `Scene Graph`.
- Switch event listeners to JavaFX’s event/binding model.

### 5️⃣ Handle threading
- Ensure UI changes occur on the JavaFX Application Thread.

### 6️⃣ Validate and test
- Confirm matching behavior and appearance.
- Compare performance where relevant.

### 7️⃣ Remove legacy Swing dependencies
- Once migration is complete, clean out hybrid wrappers.

---

## 🔗 References
- [JetUML GitHub](https://github.com/prmr/JetUML)
- [OpenJFX](https://openjfx.io)
- [Oracle Swing-JavaFX Interop Guide](https://docs.oracle.com/javafx/2/swing/swing-fx-interoperability.htm)
- [JetUML migration lessons (arXiv)](https://arxiv.org/abs/1811.04478)
- [StackOverflow migration Q&A](https://stackoverflow.com/questions/35906779/converting-from-swing-to-javafx-migration-guide)

---

## 💡 Notes
- JavaFX version: 21 (current LTS)
- Useful libraries: ControlsFX, ScenicView, JFoenix (optional)

---

## 📌 TODO
- [ ] Study JetUML’s migration commits (v1.x → v2.x).
- [ ] Try migrating a simple Swing panel to JavaFX.
- [ ] Document code patterns that help/hinder migration.
- [ ] Explore hybrid Swing + JavaFX embedding in practice.
