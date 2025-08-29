import React from "react";
import { motion } from "framer-motion";

export default function Portfolio() {
  return (
    <div className="font-sans">
      {/* Navbar */}
      <nav className="flex justify-between items-center p-4 shadow-md bg-white fixed w-full z-50">
        <h1 className="text-2xl font-bold">My Portfolio</h1>
        <ul className="flex space-x-6">
          <li><a href="#home" className="hover:text-blue-500">Home</a></li>
          <li><a href="#about" className="hover:text-blue-500">About</a></li>
          <li><a href="#projects" className="hover:text-blue-500">Projects</a></li>
          <li><a href="#skills" className="hover:text-blue-500">Skills</a></li>
          <li><a href="#contact" className="hover:text-blue-500">Contact</a></li>
        </ul>
      </nav>

      {/* Hero Section */}
      <section id="home" className="h-screen flex flex-col justify-center items-center bg-gradient-to-r from-blue-100 to-blue-300">
        <motion.h1 initial={{ opacity: 0, y: -50 }} animate={{ opacity: 1, y: 0 }} transition={{ duration: 1 }} className="text-5xl font-bold">
          Hi, I'm [Your Name]
        </motion.h1>
        <motion.p initial={{ opacity: 0 }} animate={{ opacity: 1 }} transition={{ delay: 0.5 }} className="mt-4 text-xl">
          [Your Role] | [Your Location]
        </motion.p>
      </section>

      {/* About Section */}
      <section id="about" className="min-h-screen flex flex-col justify-center items-center p-10 bg-white">
        <h2 className="text-3xl font-bold mb-4">About Me</h2>
        <p className="max-w-2xl text-center text-lg">
          Write a short professional bio here. Talk about your background, experience, and passion.
        </p>
      </section>

      {/* Projects Section */}
      <section id="projects" className="min-h-screen flex flex-col justify-center items-center p-10 bg-gray-100">
        <h2 className="text-3xl font-bold mb-6">Projects</h2>
        <div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
          {/* Example Project Card */}
          <div className="bg-white shadow-md rounded-2xl p-4">
            <h3 className="font-semibold text-xl">Project Title</h3>
            <p className="text-sm mt-2">Brief description of the project. Add a GitHub or live link below.</p>
            <a href="#" className="text-blue-500 mt-2 inline-block">View Project</a>
          </div>
        </div>
      </section>

      {/* Skills Section */}
      <section id="skills" className="min-h-screen flex flex-col justify-center items-center p-10 bg-white">
        <h2 className="text-3xl font-bold mb-6">Skills</h2>
        <div className="flex flex-wrap justify-center gap-4">
          <span className="px-4 py-2 bg-blue-200 rounded-lg">React</span>
          <span className="px-4 py-2 bg-green-200 rounded-lg">Node.js</span>
          <span className="px-4 py-2 bg-yellow-200 rounded-lg">JavaScript</span>
          <span className="px-4 py-2 bg-red-200 rounded-lg">TailwindCSS</span>
        </div>
      </section>

      {/* Contact Section */}
      <section id="contact" className="min-h-screen flex flex-col justify-center items-center p-10 bg-gray-100">
        <h2 className="text-3xl font-bold mb-6">Contact Me</h2>
        <p className="text-lg">Email: <a href="mailto:your@email.com" className="text-blue-500">your@email.com</a></p>
        <p className="text-lg">GitHub: <a href="https://github.com/yourusername" className="text-blue-500">github.com/yourusername</a></p>
        <p className="text-lg">LinkedIn: <a href="https://linkedin.com/in/yourprofile" className="text-blue-500">linkedin.com/in/yourprofile</a></p>
      </section>

      {/* Footer */}
      <footer className="p-6 bg-blue-900 text-white text-center">
        <p>© {new Date().getFullYear()} [Your Name]. All rights reserved.</p>
      </footer>
    </div>
  );
}
