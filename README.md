# Dipendra-Portfolio
import React from "react";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { Mail } from "lucide-react";

export default function Portfolio() {
  return (
    <div className="min-h-screen bg-gray-100 p-6">
      <div className="max-w-4xl mx-auto">
        <header className="flex flex-col items-center gap-4 mb-10">
          <img
            src="/profile.jpg" // Make sure to place your profile picture in the public folder with this name
            alt="Profile"
            className="w-40 h-40 rounded-full shadow-lg"
          />
          <h1 className="text-4xl font-bold">Dipendra Rathore</h1>
          <p className="text-xl text-gray-600">Computer Science Engineering Student (AI/ML)</p>
        </header>

        <section className="mb-10">
          <h2 className="text-2xl font-semibold mb-4">Skills</h2>
          <div className="grid grid-cols-2 sm:grid-cols-3 gap-4">
            {['Python', 'C++', 'DSA', 'HTML', 'CSS', 'Node.js', 'Machine Learning'].map((skill) => (
              <Card key={skill} className="text-center">
                <CardContent className="p-4 font-medium">{skill}</CardContent>
              </Card>
            ))}
          </div>
        </section>

        <section className="mb-10">
          <h2 className="text-2xl font-semibold mb-4">Projects</h2>
          <Card>
            <CardContent className="p-4">
              <h3 className="text-xl font-bold mb-2">Market Basket Analysis</h3>
              <p>
                Developed an intelligent market basket analysis system using machine learning techniques to uncover customer purchase patterns, enhancing business decision-making processes.
              </p>
            </CardContent>
          </Card>
        </section>

        <section className="mb-10">
          <h2 className="text-2xl font-semibold mb-4">Contact</h2>
          <div className="bg-white p-6 rounded-xl shadow">
            <p className="mb-2">Feel free to reach out to me via email:</p>
            <a
              href="mailto:rathoredipendra1234@gmail.com"
              className="flex items-center text-blue-600 hover:underline"
            >
              <Mail className="mr-2" /> rathoredipendra1234@gmail.com
            </a>
          </div>
        </section>

        <section>
          <h2 className="text-2xl font-semibold mb-4">Leave a Message</h2>
          <form className="bg-white p-6 rounded-xl shadow space-y-4">
            <input
              type="text"
              placeholder="Your Name"
              className="w-full border p-2 rounded"
              required
            />
            <input
              type="email"
              placeholder="Your Email"
              className="w-full border p-2 rounded"
              required
            />
            <textarea
              placeholder="Your Message"
              className="w-full border p-2 rounded"
              rows={4}
              required
            ></textarea>
            <Button type="submit">Send Message</Button>
          </form>
        </section>
      </div>
    </div>
  );
}
