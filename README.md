import { motion } from "framer-motion";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";

export default function EloirWebsite() {
  return (
    <div className="bg-white text-black min-h-screen">
      {/* HERO */}
      <section className="h-screen flex flex-col justify-center items-center text-center px-6">
        <motion.h1
          initial={{ opacity: 0, y: 40 }}
          animate={{ opacity: 1, y: 0 }}
          transition={{ duration: 0.8 }}
          className="text-6xl md:text-8xl font-bold tracking-tight"
        >
          ELOIR
        </motion.h1>
        <p className="mt-6 text-lg md:text-xl text-gray-600 max-w-xl">
          Premium streetwear crafted with purpose. Minimal design. Maximum impact.
        </p>
        <Button className="mt-10 rounded-2xl px-8 py-6 text-lg">
          Shop Collection
        </Button>
      </section>

      {/* FEATURE GRID */}
      <section className="px-6 md:px-16 py-24">
        <div className="grid grid-cols-1 md:grid-cols-3 gap-8">
          {["Premium Fabric", "Minimal Design", "Ethical Production"].map((item) => (
            <motion.div
              key={item}
              initial={{ opacity: 0, y: 30 }}
              whileInView={{ opacity: 1, y: 0 }}
              viewport={{ once: true }}
            >
              <Card className="rounded-2xl shadow-lg">
                <CardContent className="p-8 text-center">
                  <h3 className="text-2xl font-semibold">{item}</h3>
                  <p className="mt-4 text-gray-600">
                    Designed for everyday luxury with long-lasting comfort.
                  </p>
                </CardContent>
              </Card>
            </motion.div>
          ))}
        </div>
      </section>

      {/* PRODUCTS */}
      <section className="px-6 md:px-16 py-24 bg-gray-50">
        <h2 className="text-4xl md:text-5xl font-bold mb-12">Featured Drops</h2>
        <div className="grid grid-cols-1 md:grid-cols-4 gap-8">
          {[1, 2, 3, 4].map((i) => (
            <motion.div
              key={i}
              whileHover={{ scale: 1.03 }}
              className="bg-white rounded-2xl shadow-md overflow-hidden"
            >
              <div className="h-64 bg-gray-200"></div>
              <div className="p-6">
                <h3 className="font-semibold text-lg">Eloir Essential Tee</h3>
                <p className="text-gray-600 mt-2">₹1,499</p>
              </div>
            </motion.div>
          ))}
        </div>
      </section>

      {/* BRAND STORY */}
      <section className="px-6 md:px-16 py-24">
        <div className="max-w-3xl">
          <h2 className="text-4xl md:text-5xl font-bold">Designed to Last.</h2>
          <p className="mt-6 text-lg text-gray-600">
            Eloir blends modern silhouettes with premium materials to create
            timeless streetwear for those who value quality and confidence.
          </p>
        </div>
      </section>

      {/* CTA */}
      <section className="px-6 md:px-16 py-24 bg-black text-white text-center">
        <h2 className="text-4xl md:text-5xl font-bold">Join the Eloir Movement</h2>
        <p className="mt-6 text-gray-400">Luxury streetwear. No compromises.</p>
        <Button variant="secondary" className="mt-10 rounded-2xl px-8 py-6">
          Explore Now
        </Button>
      </section>

      {/* FOOTER */}
      <footer className="px-6 md:px-16 py-12 text-sm text-gray-500 flex justify-between">
        <span>© {new Date().getFullYear()} Eloir</span>
        <span>Instagram · Pinterest · Contact</span>
      </footer>
    </div>
  );
}
