<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>AIIMS B.Sc Nursing Mock Test - 100 Questions</title>
<style>
  body {
    font-family: Arial, sans-serif;
    background: #f4f4f4;
    padding: 20px;
  }
  .container {
    max-width: 1400px;
    margin: auto;
    background: white;
    padding: 25px;
    border-radius: 10px;
    box-shadow: 0 0 15px rgba(0,0,0,0.1);
  }
  h1 {
    text-align: center;
    color: #007bff;
    margin-bottom: 20px;
  }
  #timer {
    font-size: 20px;
    color: red;
    text-align: center;
    margin-bottom: 15px;
    font-weight: bold;
    user-select: none;
  }
  .sections {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 20px;
  }
  .section {
    background: #f9f9f9;
    border-radius: 8px;
    padding: 15px 18px;
    box-shadow: 0 0 6px rgba(0,0,0,0.05);
    max-height: 80vh;
    overflow-y: auto;
  }
  .section h2 {
    text-align: center;
    color: #004a99;
    margin-bottom: 12px;
    font-weight: 700;
    border-bottom: 3px solid #007bff;
    padding-bottom: 6px;
    font-size: 18px;
  }
  .question {
    margin-bottom: 16px;
  }
  .question p {
    font-weight: bold;
    margin: 0 0 6px 0;
    font-size: 14.7px;
  }
  .options label {
    display: block;
    margin-left: 18px;
    cursor: pointer;
    font-size: 14px;
    margin-bottom: 3px;
    user-select: none;
  }
  .submit-btn {
    display: block;
    margin: 30px auto 0 auto;
    padding: 12px 45px;
    font-size: 19px;
    background: #007bff;
    color: white;
    border: none;
    border-radius: 6px;
    cursor: pointer;
    transition: background 0.3s ease;
  }
  .submit-btn:hover {
    background: #0056b3;
  }
  .result {
    margin-top: 30px;
    font-size: 14px;
    font-family: monospace;
    white-space: pre-wrap;
    max-height: 400px;
    overflow-y: auto;
    border-top: 1px solid #ccc;
    padding-top: 18px;
    color: #004a99;
  }
</style>
</head>
<body>
<div class="container">
  <h1>AIIMS B.Sc Nursing Mock Test - 100 Questions</h1>
  <div id="timer">Time Left: 60:00</div>
  <form id="quiz-form">
    <div class="sections">
      <div class="section" id="bio-section">
        <h2>Biology (25)</h2>
      </div>
      <div class="section" id="chem-section">
        <h2>Chemistry (25)</h2>
      </div>
      <div class="section" id="physics-section">
        <h2>Physics (25)</h2>
      </div>
      <div class="section" id="gk-section">
        <h2>General Knowledge (25)</h2>
      </div>
    </div>
    <button type="button" class="submit-btn" onclick="submitTest()" aria-label="Submit test">Submit Test</button>
  </form>
  <div class="result" id="result" aria-live="polite"></div>
</div>

<script>
  // 100 questions divided equally - 25 per section
  // Sample questions used where available from dataset; 
  // Fill missing with placeholders or repeated questions due to length

  const biologyQuestions = [
    {q:"Human blood group is an example of:", options:["Dominance","Multiple allelism","Codominance","All of these"], answer:3},
    {q:"MOET is a method of:", options:["Fish cultivation","Birth control in humans","Cloning in sheep","Hybridization in cattle"], answer:3},
    {q:"GAATTC is the recognition site of which enzyme?", options:["Hind III","EcoRI","BamI","HaeIII"], answer:1},
    {q:"Which class of tissues seems to be the most primitive among all types of tissues?", options:["Fibers","Vessels","Parenchyma","Sieve tubes"], answer:2},
    {q:"The sequence of DNA not translated is:", options:["Introns","Exons","Cistrons","Recons"], answer:0},
    {q:"The gene that encodes for the BT protein specific to the cotton bollworm is:", options:["CryIAC","CryIIABC","CryIIAC","CryIIAB"], answer:0},
    {q:"Ranikhet disease is caused by:", options:["Bacteria","Virus","Fungus","Parasite"], answer:1},
    {q:"Mendel’s work remained unrecognized till 1900 due to all except:", options:["His work could not be widely publicised","His work was not supported with the required data","He could not provide any proof for the existence of factors","His concept of genes was not accepted by his contemporaries"], answer:1},
    {q:"Which of the following is a method of cloning in sheep?", options:["MOET","IVF","Somatic cell nuclear transfer","Hybridization"], answer:2},
    {q:"The first movement of the fetus is usually observed during which month?", options:["First","Second","Third","Fourth"], answer:1},
    {q:"The powerhouse of the cell is:", options:["Nucleus","Mitochondria","Ribosome","Golgi apparatus"], answer:1},
    {q:"The smallest bone in the human body is:", options:["Stapes","Femur","Tibia","Humerus"], answer:0},
    {q:"Which gas is released during photosynthesis?", options:["Oxygen","Carbon dioxide","Nitrogen","Hydrogen"], answer:0},
    {q:"The main function of red blood cells is to:", options:["Fight infection","Carry oxygen","Clot blood","Regulate temperature"], answer:1},
    {q:"Which part of the brain controls balance and coordination?", options:["Cerebrum","Cerebellum","Brainstem","Thalamus"], answer:1},
    {q:"The main function of the respiratory system is to:", options:["Circulate blood","Exchange gases","Digest food","Regulate temperature"], answer:1},
    {q:"Which element is essential for the formation of hemoglobin?", options:["Calcium","Iron","Magnesium","Potassium"], answer:1},
    {q:"The main function of the kidneys is to:", options:["Filter blood","Produce hormones","Digest food","Regulate temperature"], answer:0},
    {q:"The process of cell division in somatic cells is called:", options:["Meiosis","Mitosis","Binary fission","Budding"], answer:1},
    {q:"Which vitamin is important for vision?", options:["Vitamin A","Vitamin B","Vitamin C","Vitamin D"], answer:0},
    {q:"The smallest unit of life is:", options:["Tissue","Organ","Cell","Organism"], answer:2},
    {q:"Which planet is known as the Red Planet?", options:["Venus","Mars","Jupiter","Saturn"], answer:1},
    {q:"The largest mammal in the world is:", options:["Elephant","Blue whale","Giraffe","Hippopotamus"], answer:1},
    {q:"The process of photosynthesis primarily occurs in which part of the plant?", options:["Roots","Stem","Leaves","Flowers"], answer:2},
    {q:"The main function of the small intestine is to:", options:["Absorb nutrients","Digest food","Produce bile","Filter blood"], answer:0},
  ];

  const chemistryQuestions = [
    {q:"Bell metal is an alloy of:", options:["Cu, Zn, and Sn","Cu and Sn","Cu and Zn","Sn and Zn"], answer:1},
    {q:"Which of these has the highest packing efficiency?", options:["SCC","BCC","FCC","ECC"], answer:2},
    {q:"Which of these is the correct IUPAC name?", options:["Prop-2-ene","Pentan-3-al","Pentan-1-one","Pentan-2-one"], answer:3},
    {q:"Faraday’s first law of electricity states:", options:["Mass is directly proportional to the quantity of electricity","Mass is inversely proportional to the quantity of electricity","Products obtained are proportional to their equivalent weights","Products obtained are proportional to their molecular masses"], answer:0},
    {q:"Boiling point ______ as a result of intramolecular H-bonding:", options:["Increases","Decreases","Remains the same","None"], answer:1},
    {q:"The impurities associated with minerals used in metallurgy are called collectively:", options:["Slag","Gangue","Flux","Froth"], answer:1},
    {q:"Calcination is used in metallurgy for the removal of:", options:["Water and sulphide","Water and H₂S","Water and CO₂","Water and CO"], answer:2},
    {q:"If gas expands at constant temperature, then:", options:["The number of molecules increases","K.E. of the molecules increases","K.E. of the molecules decreases","K.E. of the molecules remains the same"], answer:3},
    {q:"Which of the following statements is false?", options:["Catalysts are selective","Catalysts affect the equilibrium","Catalysts affect the activation energy","Catalysts affect the mechanism"], answer:1},
    {q:"If KMnO₄ is reduced to oxalic acid in an acidic medium, then the oxidation number of Mn changes from:", options:["4 to 2","6 to 4","7 to 2","7 to 4"], answer:2},
    {q:"The chemical formula for water is:", options:["H2O","CO2","O2","H2O2"], answer:0},
    {q:"Which gas is known as laughing gas?", options:["Nitrous oxide","Carbon dioxide","Methane","Oxygen"], answer:0},
    {q:"The chemical formula for table salt is:", options:["NaCl","KCl","CaCl2","MgCl2"], answer:0},
    {q:"The chemical symbol for silver is:", options:["Ag","Au","Pb","Sn"], answer:0},
    {q:"The chemical symbol for potassium is:", options:["K","P","Na","Ca"], answer:0},
    {q:"The chemical formula for ammonia is:", options:["NH3","H2O","CO2","CH4"], answer:0},
    {q:"What is the pH of pure water?", options:["7","6","8","14"], answer:0},
    {q:"Which element has atomic number 6?", options:["Carbon","Oxygen","Nitrogen","Helium"], answer:0},
    {q:"Which type of bond is formed when electrons are shared?", options:["Ionic","Covalent","Metallic","Hydrogen"], answer:1},
    {q:"Electronegativity decreases as we move:", options:["Left to right across periodic table","Top to bottom of group","Bottom to top in group","Right to left across period"], answer:1},
    {q:"An example of amphoteric oxide is:", options:["Al2O3","CO2","SO3","Na2O"], answer:0},
    {q:"Which is the hardest natural substance?", options:["Diamond","Graphite","Quartz","Corundum"], answer:0},
    {q:"What is the oxidation state of sulfur in sulfuric acid?", options:["+6","+4","+2","-2"], answer:0},
    {q:"Which acid is known as oil of vitriol?", options:["Sulfuric acid","Nitric acid","Hydrochloric acid","Acetic acid"], answer:0},
    {q:"What is the major component of natural gas?", options:["Methane","Ethane","Propane","Butane"], answer:0},
  ];

  const physicsQuestions = [
    {q:"A thin rod of length f/3 lies along the axis of a concave mirror of focal length f. The length of the image is:", options:["f","1/2 f","2f","1/4 f"], answer:3},
    {q:"The refractive index of diamond is 2.41. What is the minimum angle of incidence to get internally reflected in a diamond?", options:["42°","35°","24.5°","48.4°"], answer:2},
    {q:"A plano-convex lens has a focal length of f = 20 cm. If its plane surface is silvered, then the new focal length will be:", options:["20 cm","5 cm","10 cm","25 cm"], answer:2},
    {q:"For an angle of minimum deviation of a prism to be equal to its refracting angle, the prism must be made of a material whose refractive index is:", options:["Lies between √2 and 1","Lies between 2 and √2","Is less than 1","Is greater than 2"], answer:1},
    {q:"In Young's double-slit experiment, the intensity is I at a point where the path difference is λ/6. If I₀ denotes the maximum intensity, then I/I₀ is equal to:", options:["3/4","1/√2","√3/2","2"], answer:0},
    {q:"At two points P and Q on the screen in Young's double-slit experiment, waves from slits S1 and S2 have a path difference of 0 and λ/4, respectively; the ratio of intensities at P and Q will be:", options:["3:2","2:1","1:2","4:1"], answer:1},
    {q:"Assuming a human pupil to have a radius of 0.25 cm and a comfortable viewing distance of 25 cm, the minimum separation between two objects that the human eye can resolve at a 500 nm wavelength is:", options:["1 μm","30 μm","100 μm","300 μm"], answer:1},
    {q:"According to Einstein's photoelectric equation, the plot of the kinetic energy of the emitted photoelectrons from a metal versus the frequency of the incident radiation gives a straight line whose slope:", options:["Depends on the nature of the metal used","Depends on the intensity of the radiation","Depends both on the intensity of the radiation and the metal used","Is the same for all metals and independent of the intensity of the radiation"], answer:3},
    {q:"The binding energy per nucleon in deuterium (1H2) and helium (2He4) atoms is 1.1 MeV and 7.0 MeV, respectively. If two deuterium atoms combine to form a single helium atom, then the energy released is:", options:["13.9 MeV","19.2 MeV","23.6 MeV","26.9 MeV"], answer:2},
    {q:"A nuclear reactor in which uranium-235 is used as fuel uses 2 kg of uranium-235 in 30 days. The power output of the reactor will be:", options:["43.5 MW","58.5 MW","69.6 MW","73.1 MW"], answer:1},
    {q:"Light travels fastest in:", options:["Vacuum","Water","Glass","Diamond"], answer:0},
    {q:"Unit of electric charge is:", options:["Coulomb","Volt","Ampere","Ohm"], answer:0},
    {q:"The force between two electric charges varies inversely as the square of distance between them. This is known as:", options:["Newton's second law","Ohm's law","Coulomb's law","Faraday's law"], answer:2},
    {q:"Velocity of sound is greatest in:", options:["Solids","Liquids","Gases","Vacuum"], answer:0},
    {q:"SI unit of power is:", options:["Watt","Joule","Newton","Volt"], answer:0},
    {q:"A projectile moves under the influence of:", options:["Elastic and magnetic force","Inertia and gravity","Electrostatic force","Gravitational and magnetic force"], answer:1},
    {q:"What is the S.I. unit of frequency?", options:["Hertz","Newton","Watt","Joule"], answer:0},
    {q:"A body in free fall near Earth's surface experiences:", options:["Zero acceleration","Constant velocity","Acceleration due to gravity","Increasing mass"], answer:2},
    {q:"In sound waves, particles of medium vibrate:", options:["Parallel to wave direction","Perpendicular to wave direction","Randomly","Not at all"], answer:0},
    {q:"Which of the following is a transverse wave?", options:["Sound","Light","Earthquake P waves","Ultrasound"], answer:1},
    {q:"Who proposed the quantum theory of light?", options:["Newton","Maxwell","Planck","Einstein"], answer:2},
    {q:"Unit of electric current is:", options:["Ampere","Ohm","Volt","Watt"], answer:0},
    {q:"The SI unit of energy is:", options:["Joule","Watt","Volt","Ampere"], answer:0},
    {q:"Which phenomenon explains the bending of light around corners?", options:["Diffraction","Reflection","Refraction","Interference"], answer:0},
    {q:"A concave mirror forms a real, inverted image when the object is at:", options:["Focus","Center of curvature","Between focus and pole","Beyond center of curvature"], answer:1}
  ];

  const gkQuestions = [
    {q:"In which state will the country’s first semiconductor fab be established?", options:["Tamil Nadu","Gujarat","Haryana","Uttarakhand"], answer:1},
    {q:"World Civil Defence Day is observed every year on:", options:["27 February","02 March","28 February","01 March"], answer:3},
    {q:"Which of the following is the capital of India?", options:["Mumbai","New Delhi","Kolkata","Chennai"], answer:1},
    {q:"The largest planet in our solar system is:", options:["Earth","Mars","Jupiter","Saturn"], answer:2},
    {q:"The currency of Japan is:", options:["Yen","Won","Dollar","Euro"], answer:0},
    {q:"The Great Wall of China was primarily built for:", options:["Trade","Defense","Tourism","Agriculture"], answer:1},
    {q:"The first man to walk on the moon was:", options:["Yuri Gagarin","Neil Armstrong","Buzz Aldrin","John Glenn"], answer:1},
    {q:"Which is the longest river in the world?", options:["Amazon","Nile","Yangtze","Mississippi"], answer:1},
    {q:"The capital of France is:", options:["Berlin","Madrid","Paris","Rome"], answer:2},
    {q:"The currency of the United States is:", options:["Dollar","Euro","Pound","Yen"], answer:0},
    {q:"Which vitamin is known as the sunshine vitamin?", options:["Vitamin A","Vitamin B","Vitamin C","Vitamin D"], answer:3},
    {q:"Which gas is a greenhouse gas?", options:["Oxygen","Methane","Nitrogen","Helium"], answer:1},
    {q:"The Taj Mahal is located in which state?", options:["Rajasthan","Uttar Pradesh","Madhya Pradesh","Haryana"], answer:1},
    {q:"Which country is the largest producer of coffee?", options:["Brazil","Colombia","India","Vietnam"], answer:0},
    {q:"Who wrote the national anthem of India?", options:["Rabindranath Tagore","Bankim Chandra Chatterjee","Sarojini Naidu","Kavi Pradeep"], answer:0},
    {q:"The International Yoga Day is observed annually on:", options:["21 June","15 August","2 October","26 January"], answer:0},
    {q:"Which animal is the national bird of India?", options:["Peacock","Eagle","Parrot","Sparrow"], answer:0},
    {q:"Nitrogen makes up approximately what percentage of the Earth's atmosphere?", options:["78%","21%","50%","10%"], answer:0},
    {q:"Who was the first president of India?", options:["Dr. Rajendra Prasad","Zakir Hussain","S Radhakrishnan","V V Giri"], answer:0},
    {q:"The currency of the United Kingdom is called:", options:["Euro","Pound Sterling","Dollar","Franc"], answer:1},
    {q:"Which city is known as the Pink City?", options:["Mumbai","Jaipur","Hyderabad","Chennai"], answer:1},
    {q:"Which planet is known as the Morning Star?", options:["Venus","Mars","Mercury","Jupiter"], answer:0},
    {q:"Who discovered penicillin?", options:["Alexander Fleming","Marie Curie","Louis Pasteur","Isaac Newton"], answer:0},
    {q:"Which is the largest continent?", options:["Asia","Africa","Europe","Antarctica"], answer:0},
    {q:"India’s first Prime Minister was:", options:["Jawaharlal Nehru","Sardar Patel","Indira Gandhi","Rajiv Gandhi"], answer:0}
  ];

  // Adjust each to exactly 25 questions if more are defined
  const bioQs = biologyQuestions.slice(0, 25);
  const chemQs = chemistryQuestions.slice(0, 25);
  const physQs = physicsQuestions.slice(0, 25);
  const gkQs = gkQuestions.slice(0, 25);

  const totalQuestions = 25 * 4; 

  const formEl = document.getElementById('quiz-form');
  const resultEl = document.getElementById('result');
  const timerEl = document.getElementById('timer');

  let time = 60 * 60; // 60 mins in seconds
  let timerInterval;

  function createQuestionHTML(questionData, sectionPrefix, index){
    const nameAttr = sectionPrefix + index;
    let html = `<div class="question"><p>${index+1}. ${questionData.q}</p>`;
    html += questionData.options.map((opt,j) =>
      `<label><input type="radio" name="${nameAttr}" value="${j}" aria-label="Option ${opt}"> ${opt}</label>`
    ).join('');
    html += '</div>';
    return html;
  }

  function renderSectionQuestions(questionsArray, sectionId, sectionPrefix){
    const container = document.getElementById(sectionId);
    container.innerHTML = container.querySelector('h2').outerHTML; // Preserve heading only
    questionsArray.forEach((q,i) => {
      container.insertAdjacentHTML('beforeend', createQuestionHTML(q, sectionPrefix, i));
    });
  }

  function renderAllQuestions(){
    renderSectionQuestions(bioQs, 'bio-section', 'bio');
    renderSectionQuestions(chemQs, 'chem-section', 'chem');
    renderSectionQuestions(physQs, 'physics-section', 'phys');
    renderSectionQuestions(gkQs, 'gk-section', 'gk');
  }

  function updateTimer() {
    const minutes = Math.floor(time/60);
    const seconds = time % 60;
    timerEl.textContent = `Time Left: ${minutes}:${seconds < 10 ? '0' : ''}${seconds}`;
    if(time <= 0){
      clearInterval(timerInterval);
      alert('Time is up! Test will be submitted automatically.');
      submitTest();
    }
    time--;
  }

  function submitTest(){
    clearInterval(timerInterval);
    let score = 0;
    let attempted = 0;
    let feedbackLines = [];

    function calcScoreAndFeedback(questionsArray, prefix){
      let sectionScore = 0;
      questionsArray.forEach((q,i) => {
        const selectedInput = document.querySelector(`input[name="${prefix}${i}"]:checked`);
        const correctText = q.options[q.answer];
        if(selectedInput){
          attempted++;
          const val = parseInt(selectedInput.value);
          if(val === q.answer){
            sectionScore += 1;
            feedbackLines.push(`${prefix.toUpperCase()} Q${i+1}: Correct (+1)`);
          } else {
            sectionScore -= 0.25;
            feedbackLines.push(`${prefix.toUpperCase()} Q${i+1}: Incorrect (-0.25)`);
          }
          feedbackLines.push(`   Correct Answer: ${correctText}`);
        } else {
          feedbackLines.push(`${prefix.toUpperCase()} Q${i+1}: Unattempted (0)`);
          feedbackLines.push(`   Correct Answer: ${correctText}`);
        }
      });
      return sectionScore;
    }

    score += calcScoreAndFeedback(bioQs, 'bio');
    score += calcScoreAndFeedback(chemQs, 'chem');
    score += calcScoreAndFeedback(physQs, 'phys');
    score += calcScoreAndFeedback(gkQs, 'gk');

    if(score < 0) score = 0;

    resultEl.textContent =
      `Total Score: ${score.toFixed(2)} / ${totalQuestions}\n` +
      `Attempted: ${attempted}\nUnattempted: ${totalQuestions - attempted}\n\n` +
      'Detailed Feedback:\n' + feedbackLines.join('\n');
    resultEl.scrollIntoView({behavior:'smooth'});
  }

  renderAllQuestions();
  timerInterval = setInterval(updateTimer, 1000);
</script>
</body>
</html>

