# Back-To-Top
Web Site back to top code
   
//back to top

let calcScrollValue = () => {
      let scrollProgress = document.getElementById("progress_t");
      let progressValue = document.getElementById("progres-value");
      let pos = document.documentElement.scrollTop;
      let calcHeight =
        document.documentElement.scrollHeight -
        document.documentElement.clientHeight;
      let scrollValue = Math.round((pos * 100) / calcHeight);
      if (pos > 100) {
        scrollProgress.style.display = "grid";
      } else {
        scrollProgress.style.display = "none";
      }
      scrollProgress.addEventListener("click", () => {
        document.documentElement.scrollTop = 0;
      });
      scrollProgress.style.background = `conic-gradient(#03cc65 ${scrollValue}%, #d7d7d7 ${scrollValue}%)`;
    };
    
    window.onscroll = calcScrollValue;
    window.onload = calcScrollValue;
