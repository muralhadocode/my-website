import { initializeApp } from "firebase/app";
import { getFirestore, collection, addDoc } from "firebase/firestore";

const firebaseConfig = {
  apiKey: "AIzaSyD4C9tBuI64pE3PlAYIGnQSSXHvi3aXXYo",
  authDomain: "idea-websitepart.firebaseapp.com",
  projectId: "idea-websitepart",
  storageBucket: "idea-websitepart.firebasestorage.app",
  messagingSenderId: "902086712735",
  appId: "1:902086712735:web:06f0aeea162e2493eb71aa",
  measurementId: "G-LH6TYGHYNF"
};

const app = initializeApp(firebaseConfig);
const db = getFirestore(app);

const btn_send = document.getElementById("btn-send");
btn_send.addEventListener("click", async function() {
  const country = document.getElementById("country").value;
  const name = document.getElementById("name").value;
  const desc_idea = document.getElementById("txt-idea").value;

  await addDoc(collection(db, "ideas"), {
    country: country,
    name: name,
    desc_idea: desc_idea,
    date: new Date()
  });

  alert("Idea sent!");
});