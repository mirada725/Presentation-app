# Interactive Presentation App

This interactive presentation app is built using [React Flow](https://reactflow.dev/) (via [@xyflow/react](https://github.com/xyflow/react)) and allows you to create, navigate, and display slide-based presentations. Each slide is rendered as a node in the flow diagram with navigation controls to move between slides using arrow keys or by clicking on the controls.

## Features

- **Slide Navigation:**  
  Navigate between slides using keyboard arrow keys and on-slide controls.
- **Interactive Flow Diagram:**  
  Visualize slides as nodes connected by directional edges.
- **Markdown Rendering:**  
  Write slide content in Markdown and render it using `react-remark`.
- **Customizable Layout:**  
  Easily update or add slides and change the navigation logic.



## Installation

1. **Clone the repository:**

   ```bash
   git clone https://github.com/your-username/your-repo.git
   cd your-repo
   ```

2. **Install dependencies:**

   ```bash
   npm install
   ```

3. **Run the development server:**

   ```bash
   npm run dev
   ```

   The app should now be running at [http://localhost:3000](http://localhost:3000) (or the port specified by your development server).

## Usage

- **Keyboard Navigation:**  
  Use the arrow keys (←, ↑, ↓, →) to navigate between slides.
  
- **Click Navigation:**  
  Click on the navigation buttons displayed on each slide to move to the corresponding slide.

- **Adding New Slides:**  
  Update the `slides.ts` file with new slide data. Each slide object should have:
  - A unique `id`.
  - A `source` string with Markdown content.
  - Optional directional properties (`left`, `up`, `down`, `right`) to specify navigation targets.

  Example slide format:
  ```js
  const slide05 = {
    id: '05',
    data: {
      left: '04',
      right: '06',
      source: `
  # Slide 5
  
  - This is a new slide.
  - Add your bullet points here.
      `,
    },
  };
  ```

## Customization

- **Styling:**  
  Modify `index.css` or add new CSS files to customize the look and feel of your presentation.
  
- **Transitions and Fit View:**  
  Adjust the `fitView` options in `App.tsx` to control the smoothness and duration of slide transitions.

- **Dynamic Slides:**  
  For a more dynamic experience, consider integrating an API or external data source to generate slide content on the fly.

## Dependencies

- [React](https://reactjs.org/)
- [@xyflow/react](https://github.com/xyflow/react) (React Flow fork)
- [react-remark](https://github.com/remarkjs/react-remark) for Markdown rendering
- [TypeScript](https://www.typescriptlang.org/) for type safety

## Troubleshooting

- **White Screen or Missing Elements:**  
  - Verify that your `index.html` includes a `<div id="root"></div>` element.
  - Ensure that parent containers of the React Flow component have defined width and height.
  
- **Styles Not Loading:**  
  - Make sure to import `@xyflow/react/dist/style.css` in your main components.
  
- **Console Errors:**  
  - Check your browser's developer console for any errors or warnings and address them accordingly.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
