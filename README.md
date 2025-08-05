<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Somaye's Portfolio</title>
  <script src="https://cdn.jsdelivr.net/npm/react@18.2.0/umd/react.production.min.js"></script>
  <script src="https://cdn.jsdelivr.net/npm/react-dom@18.2.0/umd/react-dom.production.min.js"></script>
  <script src="https://cdn.jsdelivr.net/npm/@babel/standalone@7.22.9/babel.min.js"></script>
  <script src="https://cdn.tailwindcss.com"></script>
</head>
<body>
  <div id="root"></div>
  <script type="text/babel">
    function Header() {
      return (
        <header className="bg-gradient-to-r from-blue-600 to-purple-600 text-white py-16 text-center">
          <h1 className="text-5xl font-bold mb-4">Somaye Baniasadi</h1>
          <p className="text-2xl mb-4">Front-End Developer 💻</p>
          <p className="text-lg">Passionate about building beautiful web applications</p>
        </header>
      );
    }

    function TechStack() {
      const techs = [
        { name: "React", icon: "https://cdn.jsdelivr.net/npm/simple-icons@v10/icons/react.svg" },
        { name: "JavaScript", icon: "https://cdn.jsdelivr.net/npm/simple-icons@v10/icons/javascript.svg" },
        { name: "TypeScript", icon: "https://cdn.jsdelivr.net/npm/simple-icons@v10/icons/typescript.svg" },
        { name: "Next.js", icon: "https://cdn.jsdelivr.net/npm/simple-icons@v10/icons/nextdotjs.svg" },
        { name: "Tailwind CSS", icon: "https://cdn.jsdelivr.net/npm/simple-icons@v10/icons/tailwindcss.svg" },
        { name: "Bootstrap", icon: "https://cdn.jsdelivr.net/npm/simple-icons@v10/icons/bootstrap.svg" },
        { name: "MongoDB", icon: "https://cdn.jsdelivr.net/npm/simple-icons@v10/icons/mongodb.svg" },
        { name: "GitHub", icon: "https://cdn.jsdelivr.net/npm/simple-icons@v10/icons/github.svg" },
        { name: "VS Code", icon: "https://cdn.jsdelivr.net/npm/simple-icons@v10/icons/visualstudiocode.svg" },
      ];

      return (
        <section className="py-12 bg-gray-100">
          <h2 className="text-3xl font-semibold text-center mb-8">🚀 Tech Stack</h2>
          <div className="flex flex-wrap justify-center gap-6">
            {techs.map((tech) => (
              <a
                key={tech.name}
                href={`https://${tech.name.toLowerCase().replace(" ", "")}.org`}
                target="_blank"
                rel="noopener noreferrer"
                className="transform transition-transform hover:scale-110"
              >
                <img src={tech.icon} alt={tech.name} className="w-12 h-12" />
              </a>
            ))}
          </div>
        </section>
      );
    }

    function GitHubStats() {
      return (
        <section className="py-12 bg-white">
          <h2 className="text-3xl font-semibold text-center mb-8">📊 GitHub Stats</h2>
          <div className="flex flex-col items-center gap-6">
            <img
              src="https://github-readme-streak-stats.herokuapp.com/?user=somaye56&theme=radical"
              alt="GitHub Streak"
              className="max-w-full"
            />
            <img
              src="https://github-readme-stats.vercel.app/api?username=somaye56&show_icons=true&count_private=true&include_all_commits=true&theme=radical"
              alt="GitHub Stats"
              className="max-w-full"
            />
          </div>
        </section>
      );
    }

    function Contact() {
      const contacts = [
        { name: "WhatsApp", icon: "https://cdn.jsdelivr.net/npm/simple-icons@v10/icons/whatsapp.svg", link: "https://wa.me/989356130954" },
        { name: "GitHub", icon: "https://cdn.jsdelivr.net/npm/simple-icons@v10/icons/github.svg", link: "https://github.com/somaye56" },
        { name: "Telegram", icon: "https://cdn.jsdelivr.net/npm/simple-icons@v10/icons/telegram.svg", link: "https://t.me/QSomayeh" },
        { name: "LinkedIn", icon: "https://cdn.jsdelivr.net/npm/simple-icons@v10/icons/linkedin.svg", link: "https://www.linkedin.com/in/somaye-baniasadi" },
        { name: "Email", icon: "https://cdn.jsdelivr.net/npm/simple-icons@v10/icons/gmail.svg", link: "mailto:s0maye.baniasadiii@gmail.com" },
      ];

      return (
        <section className="py-12 bg-gray-100">
          <h2 className="text-3xl font-semibold text-center mb-8">📫 Contact Me</h2>
          <div className="flex flex-wrap justify-center gap-8">
            {contacts.map((contact) => (
              <a
                key={contact.name}
                href={contact.link}
                target="_blank"
                rel="noopener noreferrer"
                className="transform transition-transform hover:scale-110"
              >
                <img src={contact.icon} alt={contact.name} className="w-12 h-12" />
              </a>
            ))}
          </div>
        </section>
      );
    }

    function App() {
      return (
        <div className="min-h-screen font-sans">
          <Header />
          <TechStack />
          <GitHubStats />
          <Contact />
          <footer className="bg-gray-800 text-white text-center py-4">
            <p>© 2025 Somaye Baniasadi. All rights reserved.</p>
          </footer>
        </div>
      );
    }

    const root = ReactDOM.createRoot(document.getElementById('root'));
    root.render(<App />);
  </script>
</body>
</html>
