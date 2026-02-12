# Website-
Create website 
import React from "react";
import { motion } from "framer-motion";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { Mail, Phone, MapPin } from "lucide-react";

export default function SandhaanPramaanWebsite() {
  return (
    <div className="min-h-screen bg-gradient-to-br from-slate-50 to-slate-100 text-gray-800">
      {/* Header */}
      <header className="bg-white shadow-sm sticky top-0 z-50">
        <div className="max-w-7xl mx-auto px-6 py-4 flex justify-between items-center">
          <div className="flex items-center gap-2">
            <img src="/mnt/data/IMG_20250615_195636_331.webp" alt="Sandhaan Pramaan Logo" className="h-10 w-10 object-contain" />
            <h1 className="text-2xl font-bold">Sandhaan Pramaan</h1>
          </div>
          <nav className="hidden md:flex gap-8 text-sm font-medium">
            <a href="#about" className="hover:text-blue-600">About</a>
            <a href="#services" className="hover:text-blue-600">Services</a>
            <a href="#whyus" className="hover:text-blue-600">Why Us</a>
            <a href="#contact" className="hover:text-blue-600">Contact</a>
          </nav>
        </div>
      </header>

      {/* Hero Section */}
      <section className="py-24 px-6 text-center">
        <motion.h2
          initial={{ opacity: 0, y: -20 }}
          animate={{ opacity: 1, y: 0 }}
          transition={{ duration: 0.6 }}
          className="text-4xl md:text-5xl font-bold mb-6"
        >
          Where Law Meets Integrity & Evidence
        </motion.h2>
        <p className="max-w-2xl mx-auto text-lg text-gray-600 mb-8">
          Sandhaan Pramaan is dedicated to delivering precise legal solutions, strategic advisory, and evidence-driven representation for individuals and businesses.
        </p>
        <Button className="rounded-2xl px-6 py-3 text-base shadow-lg">
          Book a Consultation
        </Button>
      </section>

      {/* About Section */}
      <section id="about" className="py-16 px-6 max-w-6xl mx-auto">
        <h3 className="text-3xl font-semibold mb-6 text-center">About Us</h3>
        <p className="text-gray-600 text-lg text-center max-w-3xl mx-auto">
          At Sandhaan Pramaan, we believe in strategic investigation (Sandhaan) and solid proof (Pramaan). Our firm operates through three focused divisions to serve diverse client needs:

1. Pure Legal Firm – Dedicated litigation, court representation, legal drafting, and dispute resolution services.

2. Legal + Tax Advisory – Integrated legal and taxation advisory including compliance, regulatory strategy, and structured business support.

3. Legal + AI + Compliance Boutique – A modern practice combining law, artificial intelligence tools, compliance automation, contract analytics, and regulatory technology solutions.

We deliver transparent, research-driven, and client-centric legal services with a commitment to excellence, innovation, and measurable outcomes.
        </p>
      </section>

      {/* Services Section */}
      <section id="services" className="py-16 px-6 bg-white">
        <div className="max-w-7xl mx-auto">
          <h3 className="text-3xl font-semibold mb-12 text-center">Our Services</h3>
          <div className="grid md:grid-cols-3 gap-8">
            {["Corporate & Business Advisory", "Tax & Regulatory Compliance", "Litigation & Legal Representation"].map((service, index) => (
              <Card key={index} className="rounded-2xl shadow-md hover:shadow-xl transition">
                <CardContent className="p-6">
                  <h4 className="text-xl font-semibold mb-3">{service}</h4>
                  <p className="text-gray-600">
                    Comprehensive solutions tailored to your needs with professional integrity and strategic execution.
                  </p>
                </CardContent>
              </Card>
            ))}
          </div>
        </div>
      </section>

      {/* Why Choose Us */}
      <section id="whyus" className="py-16 px-6 max-w-6xl mx-auto">
        <h3 className="text-3xl font-semibold mb-12 text-center">Why Choose Us</h3>
        <div className="grid md:grid-cols-3 gap-8 text-center">
          {["Strategic Legal Research", "Client-Centric Approach", "Transparent & Ethical Practice"].map((point, index) => (
            <motion.div
              key={index}
              whileHover={{ scale: 1.05 }}
              className="p-6 bg-white rounded-2xl shadow-md"
            >
              <h4 className="text-xl font-semibold mb-3">{point}</h4>
              <p className="text-gray-600">
                We prioritize clarity, accountability, and measurable outcomes in every engagement.
              </p>
            </motion.div>
          ))}
        </div>
      </section>

      {/* Founder Section */}
      <section id="founder" className="py-16 px-6 max-w-6xl mx-auto">
        <h3 className="text-3xl font-semibold mb-10 text-center">Founder</h3>
        <div className="bg-white rounded-2xl shadow-xl p-8 text-center max-w-3xl mx-auto">
          <h4 className="text-2xl font-bold mb-4">Adv. Saujanya Patnaik</h4>
          <p className="text-gray-600 text-lg mb-4">
            Advocate, Legal Strategist & Compliance Advisor
          </p>
          <p className="text-gray-600">
            Adv. Saujanya Patnaik leads Sandhaan Pramaan with a vision of combining traditional legal excellence with modern compliance frameworks and AI-driven legal solutions. With expertise in litigation, tax advisory, regulatory compliance, and legal research, she brings strategic clarity and result-oriented representation to clients across sectors.
          </p>
        </div>
      </section>

      {/* Contact Section */}
      <section id="contact" className="py-16 px-6 bg-white">
        <div className="max-w-5xl mx-auto text-center">
          <h3 className="text-3xl font-semibold mb-8">Contact Us</h3>
          <div className="grid md:grid-cols-3 gap-8">
            <div className="flex flex-col items-center gap-2">
              <Phone />
              <p>+91-9686479509</p>
            </div>
            <div className="flex flex-col items-center gap-2">
              <Mail />
              <p>info@sandhaanpramaan.com</p>
            </div>
            <div className="flex flex-col items-center gap-2">
              <MapPin />
              <p>India</p>
            </div>
          </div>
          <div className="mt-10">
            <Button className="rounded-2xl px-6 py-3 text-base shadow-lg">
              Schedule Appointment
            </Button>
          </div>
        </div>
      </section>

      {/* Footer */}
      <footer className="bg-gray-900 text-white py-6 text-center mt-12">
        <p>© {new Date().getFullYear()} Sandhaan Pramaan. All Rights Reserved.</p>
      </footer>
    </div>
  );
}
