# System Design Cheat Sheet

## 1. Requirements Gathering

- Ask about the constraints and the scale of the system.
- Ask about the data storage requirements.
- Ask about the availability requirements.
- Ask about the latency requirements.
- Ask about the reliability requirements.
- How many users are there?
  - How many requests per second can you handle?
  - What is the read to write ratio?
- Where are the users located?
- What are the peak and off-peak hours?

## 2. Minimum Architecture Drawing

- Sketch the important components and connections between them, but don't go into some details.
  - Client / Server
  - Application service layer (serves the requests)
  - List different services required.
  - Data Storage layer

![Minimum Architecture Drawing](./minimum-architecture.excalidraw.png)

## 3. Scale the system

- Talk about horizontal and vertical scaling.
  - Horizontal scaling: Add more servers (more machines)
  - Vertical scaling: Add more resources to the existing servers (CPU, RAM, etc.)
- Scale the client side
- Scale the server side (Application service layer and Data Storage layer)
- Scale the client side
  - Use CDN
  - Use caching
  - Use compression
  - Use load balancing
  - Use reverse proxy
- Scale the server side
  - Separate the services
  - Cache
  - Load Balancer
  - Multiple servers
  - Multiple databases

![Scale the system](./scale-minimum-architecture.excalidraw.png)

## 4. Understand the trade-offs and bottlenecks

- Talk about the trade-offs and bottlenecks of the system.
- Iterate on the architecture drawing.

## 5. Design Patterns (Optional)

- Talk about the design patterns that can be used in the system.

---

## 6. Frontend Specific - Deep dive into the Web App part

- Talk about the rendering strategy
  - Client side rendering
  - Server side rendering
  - Static site generation
- Which deployment strategy to each rendering strategy
- Monitoring and observability
- Talk about bundling optimizations
  - Tree shaking
  - Code splitting
  - Lazy loading
- Talk about image optimizations
  - Compress images
  - Use responsive images
  - Cache images
- Talk about caching strategies
  - Client side caching
  - Server side caching
  - Edge caching
  - CDN caching
  - Service worker caching / offline capabilities
- Talk about api calls optimizations and caching
  - Ex: Use caching to avoid calling the same api again and again.
  - Ex: RTK Query, React Query, etc.
- Possibility to use micro frontends
- Virtualization / Windowing for large lists

TODO: Create the drawing for the web app part
