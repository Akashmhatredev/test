props => {
  return (
    <div class={`menu-container ${props.showMenu}`}>
      <div class="overlay" />
      <div class="menu-items">
        <ul>
          <li>
            <a href="#welcome-section" onClick={props.toggleMenu}>
              HOME
            </a>
          </li>
          <li>
            <a href="#about" onClick={props.toggleMenu}>
              ABOUT
            </a>
          </li>
          <li>
            <a href="#projects" onClick={props.toggleMenu}>
              PORTFOLIO
            </a>
          </li>
          <li>
            <a href="#contact" onClick={props.toggleMenu}>
              CONTACT
            </a>
          </li>
        </ul>
        <social-links />
      </div>
    </div>
  )
}
props => {
  return (
    <React.Fragment>
      <nav id="navbar">
        <div class="nav-wrapper">
          <p class="brand">
            yago
            <strong>estévez</strong>
          </p>
          <a
            onClick={props.toggleMenu}
            class={
              props.showMenu === "active" ? "menu-button active" : "menu-button"
            }
          >
            <span />
          </a>
        </div>
      </nav>
    </React.Fragment>
  )
}
props => {
  return (
    <header id="welcome-section">
      <div class="forest" />
      <div class="silhouette" />
      <div class="moon" />
      <div class="container">
        <h1>
          <span class="line">I do</span>
          <span class="line">graphic design</span>
          <span class="line">
            <span class="color">&</span> code.
          </span>
        </h1>
        <div class="buttons">
          <a href="#projects">my portfolio</a>
          <a href="#contact" class="cta">
            get in touch
          </a>
        </div>
      </div>
    </header>
  )
}
props => {
  return (
    <section id="about">
      <div class="wrapper">
        <article>
          <div class="title">
            <h3>Who's this guy?</h3>
            <p class="separator" />
          </div>
          <div class="desc full">
            <h4 class="subtitle">My name is Yago.</h4>
            <p>
              I am a web developer and UX designer based in the beautiful west
              coast of Spain, Galicia.
            </p>
            <p>
              I really enjoy solving problems as well as making things pretty
              and easy to use. I can't stop learning new things; the more, the
              better. I also love photography, a hobby I'm taking along since
              the good old film cameras. Oh, and rice with milk; I have a
              passion for rice with milk!
            </p>
          </div>
          <div class="title">
            <h3>What does he do?</h3>
            <p class="separator" />
          </div>
          <div class="desc">
            <h4 class="subtitle">I'm a programmer.</h4>
            <p>
              For the front-end I usually work with Javascript, either
              standalone or including popular frameworks like ReactJS and VueJS.
              I also make the web pretty by using Sass, CSS and, whenever
              needed, any of their friends: Bootstrap, Bulma, etc.
            </p>
            <p>
              For the back-end I also work with Javascript (NodeJS, Express,
              MongoDB, etc). But, of course, whenever the project requires PHP,
              I do PHP as well (Wordpress, Laravel, etc).
            </p>
          </div>
          <div class="desc">
            <h4 class="subtitle">Also a designer.</h4>
            <p>
              I feel comfortable working with many Adobe products. Photoshop,
              Illustrator, InDesign, Lightroom or Xd are some kind of industry
              standards and I love working with them. I'm not limited to them,
              though: Gimp, Inkscape or Figma are also very valid applications
              that I've been working with.
            </p>
            <p>
              User interfaces, brochures, books, branding... You name it! As I
              mentioned, creating pretty things is particularly important for
              me.
            </p>
          </div>
        </article>
      </div>
    </section>
  )
}
props => {
  const tech = {
    sass: "fab fa-sass",
    css: "fab fa-css3-alt",
    js: "fab fa-js-square",
    react: "fab fa-react",
    vue: "fab fa-vuejs",
    d3: "far fa-chart-bar",
    node: "fab fa-node"
  }
  const link = props.link || "http://"
  const repo = props.repo || "http://"
  return (
    <div class="project">
      <a
        class="project-link"
        href={link}
        target="_blank"
        rel="noopener noreferrer"
      >
        <img
          class="project-image"
          src={props.img}
          alt={"Screenshot of " + props.title}
        />
      </a>
      <div class="project-details">
        <div class="project-tile">
          <p class="icons">
            {props.tech.split(" ").map(t => (
              <i class={tech[t]} key={t} />
            ))}
          </p>
          {props.title}{" "}
        </div>
        {c.children}
        <div class="buttons">
          <a href={repo} target="_blank" rel="noopener noreferrer">
            View source <i class="fas fa-external-link-alt" />
          </a>
          <a href={link} target="_blank" rel="noopener noreferrer">
            Try it Live <i class="fas fa-external-link-alt" />
          </a>
        </div>
      </div>
    </div>
  )
}
props => {
  return (
    <section id="projects">
      <div class="projects-container">
        <div class="heading">
          <h3 class="title">My Works</h3>
          <p class="separator" />
          <p class="subtitle">
            Here's a list of <u>most</u> of the projects I've been working on
            lately. All of these were built during my coding camp adventure on{" "}
            <a
              href="https://www.freecodecamp.org/"
              target="_blank"
              rel="noopener noreferrer"
            >
              freeCodeCamp
            </a>
            , where I've been coding for almost 7 months non-stop until I
            completed all the projects required to get my Full-Stack Developer
            certification.
          </p>
        </div>
        <div class="projects-wrapper">
          <project
            title="Anonymous Message Board."
            img={
              "https://raw.githubusercontent.com/yagoestevez/fcc-portfolio/master/src/Components/Projects/Images/AnonMsgBoard.jpg"
            }
            tech="js css react node"
            link="https://yagoestevez-anon-msg-board.glitch.me/"
            repo="https://github.com/yagoestevez/anonymous-message-board"
          >
            <small>
              Built using Node, Express, MongoDB, CSS + Bulma, React.js and
              React Router.
            </small>
            <p>
              This is a full-stack website that I made which lets the users read
              and post anonymous messages and replies.
            </p>
          </project>
          <project
            title="Stock Price Checker."
            img={
              "https://raw.githubusercontent.com/yagoestevez/fcc-portfolio/master/src/Components/Projects/Images/StockPriceChecker.jpg"
            }
            tech="js node css"
            link="https://yagoestevez-stock-price-checker.glitch.me/"
            repo="https://github.com/yagoestevez/fcc-stock-price-checker"
          >
            <small>
              Built using Node, Express, MongoDB, JS + jQuery + Axios, CSS +
              Bootstrap and Pug.
            </small>
            <p>
              Another full-stack website to check the current value of any
              requested stock in the market.
            </p>
          </project>
          <project
            title="Personal Library."
            img={
              "https://raw.githubusercontent.com/yagoestevez/fcc-portfolio/master/src/Components/Projects/Images/PersonalLibrary.jpg"
            }
            tech="js node css"
            link="https://yagoestevez-personal-library.glitch.me/"
            repo="https://github.com/yagoestevez/fcc-personal-library"
          >
            <small>
              Built using Node, Express, MongoDB, JS + jQuery, CSS + Bootstrap
              and Pug.
            </small>
            <p>
              A full-stack website to store book titles and comments to each
              book into a remote database.
            </p>
          </project>
          <project
            title="Issue Tracker."
            img={
              "https://raw.githubusercontent.com/yagoestevez/fcc-portfolio/master/src/Components/Projects/Images/IssueTracker.jpg"
            }
            tech="js node css"
            link="https://yagoestevez-issue-tracker.glitch.me/"
            repo="https://github.com/yagoestevez/fcc-issue-tracker"
          >
            <small>
              Built using Node, Express, MongoDB, JS + jQuery, CSS + Bootstrap
              and Pug.
            </small>
            <p>
              Yet another full-stack app to save and manage technical issues to
              be fixed.
            </p>
          </project>
          <project
            title="Metric-Imperial Converter."
            img={
              "https://raw.githubusercontent.com/yagoestevez/fcc-portfolio/master/src/Components/Projects/Images/MetricImperialConverter.jpg"
            }
            tech="js node css"
            link="https://yagoestevez-metric-imperial-converter.glitch.me/"
            repo="https://github.com/yagoestevez/fcc-metric-imperial-converter/"
          >
            <small>
              Built using Node, Express, JS + jQuery, CSS + Bootstrap and Pug.
            </small>
            <p>
              Another full-stack for converting values from the Internation
              System of Units (Metric) into the imperial units.
            </p>
          </project>
          <project
            title="URL Shortener Microservice."
            img={
              "https://raw.githubusercontent.com/yagoestevez/fcc-portfolio/master/src/Components/Projects/Images/Cortala.jpg"
            }
            tech="js node css"
            link="https://cortala.glitch.me/example"
            repo="https://github.com/yagoestevez/cortala"
          >
            <small>Built using Node, Express, CSS + Bootstrap and Pug.</small>
            <p>
              A microservice which takes a raw URL and makes it a short link to
              make it easy to sent it through the Internet.
            </p>
          </project>
          <project
            title="Exercise Tracker."
            img={
              "https://raw.githubusercontent.com/yagoestevez/fcc-portfolio/master/src/Components/Projects/Images/ExerciseTracker.jpg"
            }
            tech="js vue node css"
            link="https://yagoestevez-exercise-tracker.glitch.me"
            repo="https://github.com/yagoestevez/exercise-tracker"
          >
            <small>
              Built using Node, Express, VueJS + Vue Router and CSS + Bootstrap.
            </small>
            <p>
              A service which lets the users save their daily exercise (or
              anything) into a log for them to check it later.
            </p>
          </project>
          <project
            title="Bar Chart."
            img={
              "https://raw.githubusercontent.com/yagoestevez/fcc-portfolio/master/src/Components/Projects/Images/BarChart.jpg"
            }
            tech="js d3 css"
            link="https://codepen.io/yagoestevez/full/wxjmrB/"
            repo="https://github.com/yagoestevez/fcc-barchart"
          >
            <small>Built using CSS, JS and D3.js.</small>
            <p>A bar chart representing the evolution of the US GDP.</p>
          </project>
          <project
            title="Treemap Diagram."
            img={
              "https://raw.githubusercontent.com/yagoestevez/fcc-portfolio/master/src/Components/Projects/Images/TreemapDiagram.jpg"
            }
            tech="js d3 css"
            link="https://codepen.io/yagoestevez/full/bjZygz/"
            repo="https://github.com/yagoestevez/fcc-treemap-diagram"
          >
            <small>Built using CSS, JS and D3.js.</small>
            <p>
              A treemap diagram representing groups of pledges and sales from a
              particular category.
            </p>
          </project>
          <project
            title="Choropleth Map."
            img={
              "https://raw.githubusercontent.com/yagoestevez/fcc-portfolio/master/src/Components/Projects/Images/ChoroplethMap.jpg"
            }
            tech="js d3 css"
            link="https://codepen.io/yagoestevez/full/NBeaWK/"
            repo="https://github.com/yagoestevez/fcc-choropleth-map"
          >
            <small>Built using CSS, JS and D3.js.</small>
            <p>
              A choropleth map representing the educational attainment by county
              in the U.S.
            </p>
          </project>
          <project
            title="Random Quoting Machine."
            img={
              "https://raw.githubusercontent.com/yagoestevez/fcc-portfolio/master/src/Components/Projects/Images/QuotingMachine.jpg"
            }
            tech="js vue css"
            link="https://codepen.io/yagoestevez/full/bxgEyd/"
            repo="https://github.com/yagoestevez/random-quoting-machine"
          >
            <small>Built using VueJS, Axios and CSS + Bootstrap.</small>
            <p>
              A random quoting app which retrieves pictures and quotes from two
              different APIs.
            </p>
          </project>
          <project
            title="Calculator."
            img={
              "https://raw.githubusercontent.com/yagoestevez/fcc-portfolio/master/src/Components/Projects/Images/Calculator.jpg"
            }
            tech="js react css"
            link="https://codepen.io/yagoestevez/full/ERVONM/"
            repo="https://github.com/yagoestevez/the-calcoolator"
          >
            <small>Built using React and CSS.</small>
            <p>
              A project on which I built a virtual calculator with its usual
              features.
            </p>
          </project>
          <project
            title="Pomodoro Timer."
            img={
              "https://raw.githubusercontent.com/yagoestevez/fcc-portfolio/master/src/Components/Projects/Images/TomateTimer.jpg"
            }
            tech="js react css"
            link="https://codepen.io/yagoestevez/full/dqJGVa"
            repo="https://github.com/yagoestevez/tomate-time"
          >
            <small>Built using React, CSS and lots of SVG.</small>
            <p>
              A cute and animated Pomodoro clock to help the users improve their
              productivity.
            </p>
          </project>
          <project
            title="TicTacToe Game."
            img={
              "https://raw.githubusercontent.com/yagoestevez/fcc-portfolio/master/src/Components/Projects/Images/TicTacToe.jpg"
            }
            tech="js react css"
            link="https://codepen.io/yagoestevez/full/KRevzB/"
            repo="https://github.com/yagoestevez/TicTacToe"
          >
            <small>Built using React, CSS and SVG.</small>
            <p>
              A TicTacToe game with a basic AI algorithm made for the legacy
              front-end projects on FreeCodeCamp.
            </p>
          </project>
          <project
            title="Twitch Clone."
            img={
              "https://raw.githubusercontent.com/yagoestevez/fcc-portfolio/master/src/Components/Projects/Images/Twitch.jpg"
            }
            tech="js vue sass"
            link="https://codepen.io/yagoestevez/full/xjwVPq/"
          >
            {/* repo="https://github.com/yagoestevez/TicTacToe"> */}
            <small>Built using VueJS, Axios and Scss.</small>
            <p>
              Simple Twitch clone using the new Twitch Helix API and made for
              the legacy front-end projects on FreeCodeCamp.
            </p>
          </project>
          <project
            title="Weather App."
            img={
              "https://raw.githubusercontent.com/yagoestevez/fcc-portfolio/master/src/Components/Projects/Images/WeatherApp.jpg"
            }
            tech="js vue css"
            link="https://codepen.io/yagoestevez/full/zWbGmZ/"
          >
            {/* repo="https://github.com/yagoestevez/TicTacToe"> */}
            <small>Built using VueJS, Axios and CSS.</small>
            <p>
              App that present the users with the current local weather for
              their location.
            </p>
          </project>
          <project
            title="Tribute."
            img={
              "https://raw.githubusercontent.com/yagoestevez/fcc-portfolio/master/src/Components/Projects/Images/Tribute.jpg"
            }
            tech="js sass"
            link="https://codepen.io/yagoestevez/full/aaaOxL/"
            repo="https://github.com/yagoestevez/tribute-to-aaron-swartz"
          >
            <small>Built using vanilla Javascript and Scss.</small>
            <p>
              Tribute page to Aaron Swartz, a static website built with SCSS and
              plain Javascript.
            </p>
          </project>
          <project
            title="Survey Form."
            img={
              "https://raw.githubusercontent.com/yagoestevez/fcc-portfolio/master/src/Components/Projects/Images/SurveyForm.jpg"
            }
            tech="js sass"
            link="https://codepen.io/yagoestevez/full/bjVgjX/"
            repo="https://github.com/yagoestevez/membership-form"
          >
            <small>Built using vanilla Javascript and Scss.</small>
            <p>An animated survey form.</p>
          </project>
          <project
            title="Landing Page Example."
            img={
              "https://raw.githubusercontent.com/yagoestevez/fcc-portfolio/master/src/Components/Projects/Images/LandingPage.jpg"
            }
            tech="js sass"
            link="https://codepen.io/yagoestevez/full/pOBLeK/"
            repo="https://github.com/yagoestevez/tomate-timer-landing-page"
          >
            <small>Built using vanilla Javascript and Scss.</small>
            <p>
              A landing page for the Pomodoro Timer I made (shown previously in
              this section).
            </p>
          </project>
          <project
            title="Technical Documentation Page."
            img={
              "https://raw.githubusercontent.com/yagoestevez/fcc-portfolio/master/src/Components/Projects/Images/Documentify.jpg"
            }
            tech="js react css"
            link="https://codepen.io/yagoestevez/full/QxOLKX/"
            repo="https://github.com/yagoestevez/documentify"
          >
            <small>Built using React and CSS.</small>
            <p>
              A technical documentation page made for a little React library I
              published on NPM.
            </p>
          </project>
        </div>
      </div>
    </section>
  )
}
props => {
  return (
    <section id="contact">
      <div class="container">
        <div class="heading-wrapper">
          <div class="heading">
            <p class="title">
              Want to <br />
              contact me?
            </p>
            <p class="separator" />
            <p class="subtitle">
              Please, use the form below or send an email to {""}
              <span class="mail">
                web
                <i class="fas fa-at at" />
                yagoestevez
                <i class="fas fa-circle dot" />
                com
              </span>
              :
            </p>
          </div>
          <social-links />
        </div>
        <form id="contact-form" action="#">
          <input placeholder="Name" name="name" type="text" required />
          <input placeholder="Email" name="email" type="email" required />
          <textarea placeholder="Message" type="text" name="message" />
          <input class="button" id="submit" value="Submit" type="submit" />
        </form>
      </div>
    </section>
  )
}
props => {
  return (
    <footer>
      <div class="wrapper">
        <h3>THANKS FOR VISITING</h3>
        <p>© {new Date().getFullYear()} Yago Estévez.</p>
        <social-links />
      </div>
    </footer>
  )
}
props => {
  return (
    <div class="social">
      <a
        href="https://twitter.com/yagoestevez"
        target="_blank"
        rel="noopener noreferrer"
        title="Link to author's Twitter profile"
      >
        {" "}
        <i class="fab fa-twitter" />
      </a>
      <a
        id="profile-link"
        href="https://github.com/yagoestevez"
        target="_blank"
        rel="noopener noreferrer"
        title="Link to author's GitHub Profile"
      >
        {" "}
        <i class="fab fa-github" />
      </a>
      <a
        href="https://codepen.io/yagoestevez"
        target="_blank"
        rel="noopener noreferrer"
        title="Link to author's Codepen Profile"
      >
        {" "}
        <i class="fab fa-codepen" />
      </a>
    </div>
  )
} // export component
export default {
  name: "app",
  mounted() {
    const navbar = document.querySelector("#navbar")
    const header = document.querySelector("#welcome-section")
    const forest = document.querySelector(".forest")
    const silhouette = document.querySelector(".silhouette")
    let forestInitPos = -300

    window.onscroll = () => {
      let scrollPos =
        document.documentElement.scrollTop || document.body.scrollTop

      if (scrollPos <= window.innerHeight) {
        silhouette.style.bottom = `${parseInt(scrollPos / 6)}px`
        forest.style.bottom = `${parseInt(forestInitPos + scrollPos / 6)}px`
      }

      if (scrollPos - 100 <= window.innerHeight)
        header.style.visibility =
          header.style.visibility === "hidden" && "visible"
      else header.style.visibility = "hidden"
      if (scrollPos + 100 >= window.innerHeight)
        navbar.classList.add("bg-active")
      else navbar.classList.remove("bg-active")
    }

    ;(function navSmoothScrolling() {
      const internalLinks = document.querySelectorAll('a[href^="#"]')

      for (let i in internalLinks) {
        if (internalLinks.hasOwnProperty(i)) {
          internalLinks[i].addEventListener("click", e => {
            e.preventDefault()
            document.querySelector(internalLinks[i].hash).scrollIntoView({
              block: "start",
              behavior: "smooth"
            })
          })
        }
      }
    })()
  },
  render() {
    return (
      <React.Fragment>
        <menu toggleMenu={this.toggleMenu} showMenu={this.menuState} />
        <nav toggleMenu={this.toggleMenu} showMenu={this.menuState} />
        <header />
        <about />
        <projects />
        <contact />
        <footer />
      </React.Fragment>
    )
  }
}
