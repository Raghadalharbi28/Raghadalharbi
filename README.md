import { motion } from 'framer-motion';
import { useInView } from 'framer-motion';
import { useRef } from 'react';
import { Phone, MapPin, Clock } from 'lucide-react';
import { useLanguage } from '@/contexts/LanguageContext';

const Contact = () => {
  const { t } = useLanguage();
  const ref = useRef(null);
  const isInView = useInView(ref, { once: true, margin: "-100px" });

  const contactItems = [
    {
      icon: Phone,
      label: t.contact.phone,
      value: "030 7568020",
      href: "tel:0307568020",
      multiLine: false,
    },
    {
      icon: MapPin,
      label: t.contact.address,
      value: "Manteuffelstraße 65, 12103 Berlin",
      href: "https://maps.google.com/?q=Manteuffelstraße+65,+12103+Berlin",
      multiLine: false,
    },
    {
      icon: Clock,
      label: t.contact.hours,
      value: [t.contact.hoursWeekdays, t.contact.hoursFriday, t.contact.hoursWeekend],
      href: null,
      multiLine: true,
    },
  ];

  return (
    <section id="contact" className="py-24" ref={ref}>
      <div className="container mx-auto px-4">
        <div className="max-w-6xl mx-auto">
          {/* Header */}
          <motion.div
            initial={{ opacity: 0, y: 30 }}
            animate={isInView ? { opacity: 1, y: 0 } : {}}
            transition={{ duration: 0.6 }}
            className="text-center mb-16"
          >
            <span className="inline-block text-secondary font-medium mb-4">
              {t.contact.title}
            </span>
            <h2 className="text-3xl md:text-4xl font-display font-bold text-foreground mb-4">
              {t.contact.subtitle}
            </h2>
          </motion.div>

          <div className="grid lg:grid-cols-2 gap-12">
            {/* Contact Info */}
            <motion.div
              initial={{ opacity: 0, x: -50 }}
              animate={isInView ? { opacity: 1, x: 0 } : {}}
              transition={{ duration: 0.6, delay: 0.2 }}
              className="space-y-6"
            >
              {contactItems.map((item, index) => {
                const Icon = item.icon;
                const Content = (
                  <div className="flex items-start gap-4 bg-card p-6 rounded-2xl shadow-card hover:shadow-card-hover transition-all duration-300">
                    <div className="w-14 h-14 bg-gradient-hero rounded-xl flex items-center justify-center shrink-0">
                      <Icon className="w-6 h-6 text-primary-foreground" />
                    </div>
                    <div>
                      <div className="text-sm text-muted-foreground mb-1">{item.label}</div>
                      {item.multiLine ? (
                        <div className="space-y-1">
                          {(item.value as string[]).map((line, i) => (
                            <div key={i} className="text-base font-semibold text-foreground">{line}</div>
                          ))}
                        </div>
                      ) : (
                        <div className="text-lg font-semibold text-foreground">{item.value as string}</div>
                      )}
                    </div>
                  </div>
                );

                return (
                  <motion.div
                    key={index}
                    initial={{ opacity: 0, y: 20 }}
                    animate={isInView ? { opacity: 1, y: 0 } : {}}
                    transition={{ duration: 0.4, delay: 0.3 + index * 0.1 }}
                  >
                    {item.href ? (
                      <a href={item.href} target="_blank" rel="noopener noreferrer" className="block">
                        {Content}
                      </a>
                    ) : (
                      Content
                    )}
                  </motion.div>
                );
              })}
            </motion.div>

            {/* Google Map */}
            <motion.div
              initial={{ opacity: 0, x: 50 }}
              animate={isInView ? { opacity: 1, x: 0 } : {}}
              transition={{ duration: 0.6, delay: 0.4 }}
              className="relative rounded-2xl overflow-hidden shadow-card h-[400px]"
            >
              <iframe
                src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2429.9!2d13.3865!3d52.4555!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x47a84fd91e7a4c3d%3A0x0!2sManteuffelstra%C3%9Fe%2065%2C%2012103%20Berlin!5e0!3m2!1sen!2sde!4v1"
                width="100%"
                height="100%"
                style={{ border: 0 }}
                allowFullScreen
                loading="lazy"
                referrerPolicy="no-referrer-when-downgrade"
                title="AGG Location"
              />
            </motion.div>
          </div>
        </div>
      </div>
    </section>
  );
};

export default Contact;
