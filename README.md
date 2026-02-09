## 🧱 Code Structure

The application is intentionally structured in small, readable parts to support learning
and long-term maintainability.

### 🪟 App Lifecycle

The app follows a clear setup flow inside the `PomotatoApp` class:

1. **Window setup**  
   Handles window size, resize behavior, and basic configuration.

2. **State setup**  
   Manages the timer state (focus/break, running, remaining time).

3. **UI building**  
   The interface is built in small, dedicated methods (header, timer, controls, settings).

4. **Event binding**  
   Mouse hover events control window expansion to keep the app unobtrusive while studying.

5. **Rendering**  
   UI updates are centralized in a single render method.

---

### 🧠 Key Design Decisions

- **Small window by default**  
  The app starts in a compact mode to reduce distraction.

- **Hover-based expansion**  
  Controls appear only when needed by expanding the window on mouse hover.

- **Clear separation of concerns**  
  UI layout, state management, and timer logic are handled in separate methods.

- **Readable over clever**  
  The code prioritizes clarity and learning over abstraction or optimization.

---

### 📂 Internal Structure (app.py)

- `_setup_window()` – window size & behavior  
- `_setup_state()` – timer & UI state  
- `_build_*()` – UI construction  
- `_bind_events()` – mouse hover handling  
- `_render_time()` – UI updates  
- `_tick()` – timer heartbeat  
- `start / pause / reset / switch_mode()` – user actions  

This structure makes it easy to add features gradually without breaking existing behavior.

---

> This project favors steady progress and understanding over speed or perfection 🍅